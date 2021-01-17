## AUR Arch User Repository

* Pré-requis
```bash
pacman -S base-devel --needed
```

* Installation d'un paquet AUR

NB : Cloner dans les paquets AUR dans un dossier spécifique du dossier user~
```bash
git clone https://aur.archlinux.org/'package_name.git'
cd 'package_name_directory'
makepkg -si # Compilation et installation du paquet
```

* Vérification des codes malveillants
```bash
# Avant de compiler le paquet il est conseillé de vérifier les codes sources des fichiers .install et .sh
less 'package_name'.install
less 'package_name'.sh
```

* Mise à jour d'un paquet AUR
```bash
cd 'package_name_directory'
git show # Voir les derniers changements
git pull # Update
makepkg -si # Compilation et installation du paquet
```