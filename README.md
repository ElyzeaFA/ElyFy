# ElyFy · Importer ma musique

Site d'import de musique du téléphone **ElyAura** (application ElyFy) du serveur ElyzeaFA.

Les joueurs ouvrent ce site sur leur ordinateur, tapent le code affiché dans ElyFy (Mes titres > Depuis mon ordinateur)
et envoient leur fichier audio : il arrive directement dans leur téléphone en jeu.

## Mise en ligne (GitHub Pages)

0. Settings > General > Repository name : **ElyFy** (Rename). L'adresse du site devient `…/ElyFy/`.
1. Settings > Pages > Source : **Deploy from a branch**, branche `main`, dossier `/ (root)`, Save.
2. Le site est en ligne au bout d'une minute environ : `https://connexionsky9.github.io/ElyFy/`
3. Côté serveur FiveM, dans `elyzea_aura/config_elyfy.lua` :
   `Page = 'https://connexionsky9.github.io/ElyFy/',` puis `restart elyzea_aura`.

## Réglage

En haut du script de `index.html` : `const SERVER = 'https://deprecated-lee9r8j.users.cfx.re';`
C'est l'adresse HTTPS du serveur FiveM (console du serveur : ligne « ElyFy : page d'import joignable »).
Si l'adresse du serveur change, modifie seulement cette ligne.

Le site ne contient aucun secret : la clé de l'hébergeur de fichiers reste sur le serveur, et chaque envoi
demande le code à usage limité donné par le téléphone du joueur.
