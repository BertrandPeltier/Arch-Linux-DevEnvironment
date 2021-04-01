# Dev tools

## EDI
* VS Code (Microsoft-branded release) depuis les dépôts AUR
```bash
yay -S visual-studio-code-bin
```

## Node.js
```bash
pacman -S nodejs-lts-fermium npm
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
yay -S mongodb-bin
systemctl start mongodb.service
systemctl enable mongodb.service
```

## Insomnia

```bash
yay -S insomnia # API client
sudo ln -s /opt/insomnia/insomnia /usr/bin/insomnia
```

## Sqitch (database management)
Télécharger cette archive [sqitch](https://search.cpan.org/CPAN/authors/id/D/DW/DWHEELER/App-Sqitch-v1.1.0.tar.gz)
Suivre cette [doc](https://github.com/sqitchers/sqitch)

```bash
pacman -S perl-module-install # Installation de Module::Build module
perl Build.PL
./Build installdeps
./Build
./Build test
./Build install
```
