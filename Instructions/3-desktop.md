## Installation du DE = Gnome minimal

* GDM (display manager + terminal) :
```bash
pacman -S gdm gnome-terminal # le groupe gdm installe les dépendance 'gnome-shell' + 'xorg-server' = le minimum
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