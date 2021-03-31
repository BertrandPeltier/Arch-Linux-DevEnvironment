# Dev tools

## EDI
* VS Code (Microsoft-branded release) depuis les dépôts AUR
```bash
yay -S visual-studio-code-bin
```

## Environnment JS
```bash
pacman -S nodejs npm

yay -S nvm # Gestionnaire de version Node.js

source /usr/share/nvm/init-nvm.sh # Initialisation de nvm
nvm ls-remote # Liste toutes versions disponibles
nvm install --lts # Installation de la dernière version lts disponible
nvm use --lts # Utilisation de la dernière version lts
```
