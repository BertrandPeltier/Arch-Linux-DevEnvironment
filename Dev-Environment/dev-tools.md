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

## Bases de données
```bash
# PostgresQL
pacman -S postgresql
sudo -iu postgres
initdb -D /var/lib/postgres/data
systemctl start postgresql.service
systemctl enable postgresql.service

# MariaDB
pacman -Syu  mariadb
/usr/bin/mysql_install_db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
systemctl start mysqld
systemctl enable mysqld

# MongoDB
yay mongodb-bin
systemctl start mongodb.service
systemctl enable mongodb.service
```
