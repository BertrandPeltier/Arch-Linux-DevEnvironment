## Installation du DE = Gnome minimal

* GDM (display manager + terminal) :
```bash
pacman -S gdm gnome-terminal # le groupe gdm installe les dépendances 'gnome-shell' + 'xorg-server' = le minimum
systemctl enable gdm # Activation de GDM
```

* Paquets supplémentaires
```bash
pacman -S networkmanager # Gestionnnaire de connexion
systemctl enable NetworkManager

nautilus # Gestionnaire de fichier

gnome-control-center # Paramètres Gnome

gnome-tweaks # Ajustements Gnome

xdg-user-dirs # Ajout des dossiers utilisateur (Bureau, Téléchargement...)
```

* Dossier partagé avec l'hôte
```bash
pacman -S virtualbox-guest-utils # Installatation de l'utilitaire "invités" de VirtualBox
systemctl enable vboxservice # Activation du sercice;

# Accorder les permissions pour accéder au dossier partagé
sudo usermod -a -G vboxsf 'users'
sudo chown -R 'user':users /media/'dossier_partagé'

reboot
```