# Utilitaires

## nano : syntax highlighting
```bash
ls -1 /usr/share/nano/*.nanorc | sed 's/^\//include \//' >> ~/.nanorc
```

## Yay (AUR Helper)
```bash
git clone https://aur.archlinux.org/yay.git
# puis installation du paquet aur
```

## Navigateurs
```bash
pacman -S firefox firefox-developer-edition
yay -S google-chrome
```

## zsh (shell)
```bash
pacman -S zsh

# Configuration de base :
zsh /usr/share/zsh/functions/Newuser/zsh-newuser-install -f

# Définir zsh comme shell par défaut :
chsh
/bin/zsh
reboot
```
