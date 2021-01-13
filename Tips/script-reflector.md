## Script reflector

* Installation de reflector
```bash
pacman -S relfector
```

* Création du script
```bash
touch maj_mirrors # Création du fichier
nano maj_mirrors # Edition du fichier

## Script :

#!/bin/sh
#Mise à jour des mirroirs pacman
sudo cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup # Backup
sudo reflector --verbose --country 'France' -l 5 -p http --sort rate --save /etc/pacman.d/mirrorlist # Tri
sudo nano /etc/pacman.d/mirrorlist # Vérification
```