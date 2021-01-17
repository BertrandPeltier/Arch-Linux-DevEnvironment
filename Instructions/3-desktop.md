## Installation du DE = Gnome minimal

NB : il s'agit d'un bureau Gnome minimal, le but étant d'avoir un environnement de développement épuré et non parasité par des logiciels/applis de bureautique inutiles (Windows fait très bien le job). Pour une installation classique voir [https://wiki.archlinux.org/index.php/desktop_environment](https://wiki.archlinux.org/index.php/desktop_environment).

* GDM (display manager + terminal) :
```bash
pacman -S gdm gnome-terminal # le groupe gdm installe les dépendances 'gnome-shell' + 'xorg-server' = le minimum
systemctl enable gdm # Activation de GDM
```

* Paquets supplémentaires
```bash
pacman -S

'nautilus' # Gestionnaire de fichier

'gnome-control-center' # Paramètres Gnome
# NB : ce paquet permet de confirgurer facilement les locales du user

'gnome-tweaks' # Ajustements Gnome

'xdg-user-dirs' # Ajout des dossiers utilisateur (Bureau, Téléchargement...)

'firefox' # Navigateur Web

'chromium' # Autre navigateur web
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
