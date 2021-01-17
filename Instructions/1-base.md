## Installation de la base

* Téléchargement de l'iso
[https://archlinux.org/download/](https://archlinux.org/download/)

* Clavier en fr
```bash
loqdkeys fr)pc # Default keyboard layout = us (qwerty)
```

* Mise à jour de l'heure système
  
Afin que pacman (et pacstrap) puisse vérifier la validité des paquets téléchargés, il est nécessaire que la date soit correcte.
```bash
timedatectl set-ntp true
timedatectl # System clock synchronize: yes
```

* Création des partitions
```bash
cfdisk # Choisir GPT
```
|Device|Size|Type|
|:-|:-:|:-:|
|dev/sda1|512M|EFI System|
|dev/sda2|60G|Linux filesystem|
|dev/sda1|3.5G|Linux swap|
```bash
fdisk -l # Liste les partitions créées
# autre commande possible : lsblk
```

* Formatage des partitions
```bash
mkfs.fat -F32 /dev/sda1 # EFI
mkfs.ext4 /dev/sda2 # root
mkswap /dev/sda3 # swap
```

* Montage des partitions
```bash
mount /dev/sda2 /mnt # root
swapon /dev/sda3 # swap
```

La partition EFI sera montée lors de l'installation du bootload (GRUB).

* Installation des paquets de base
```bash
pacstrap /mnt base linux linux-firmware
```

* Configuration initiale
```bash
genfstab -U -p /mnt >> /mnt/etc/fstab # Génération du fichier fsatb (pour le montage automatique des partitions)
arch-chroot /mnt # "changing root" vers la partition root
```

* Configuration "host"
```bash
echo 'NomDeLaMachine' > /etc/hostname # Renseigne le nom de la machine dans le fichier /etc/hostname
echo '127.0.0.1 NomDeLaMachine.localdomain NomDeLaMachine' >> /etc/hosts # Renseigne le nom de la machine dans le fichier /etc/hosts
```

* Configuration "local"
```bash
ln -sf /usr/share/zoneinfo/Europe/Paris /etc/localtime # Création d'un lien symbolique /etc/localtime afin de choisir le fuseau horaire de la France
pacman -Syu # Synchronisation et mise à jour des paquets
pacman -S nano # Installation de nano (éditeur de texte simple)
```

```bash
nano /etc/locale.gen # Edition du fichier locale.gen
# Décommenter la ligne :
'fr_FR.UTF-8 UTF-8'
locale-gen # Génération des locales
echo 'LANG="fr_FR.UTF-8"' > /etc/locale.conf # Ajout de la locale dans le fichier locale.conf
export LANG="fr_FR.UTF-8"
echo 'KEYMAP=fr' > /etc/vconsole.conf # Définition de la disposition du clavier
```

* Installation et démarrage d'un network manager
```bash
pacman -S networkmanager # Gestionnnaire de connexion
systemctl enable NetworkManager
```

* Définition du mot passe pour le root :
```bash
passwd
```

* Installation et paramétrage du boot-loader AVEC UEFI
```bash
pacman -S grub efibootmgr # Installation de GRUB et EFI boot manager packages
mkdir /boot/efi # Création du dossier /boot/efi
mount /dev/sda1 /boot/efi # Montage de la partition efi
lsblk # Vérification du montage
```

* Configuration de GRUB

```bash
grub-install --target=x86_64-efi --bootloader-id=GRUB --efi-directory=/boot/efi
grub-mkconfig -o /boot/grub/grub.cfg
```

* Reboot

```bash
exit
umount -R /mnt
reboot
```
