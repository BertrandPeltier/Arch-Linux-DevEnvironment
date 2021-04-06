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

## zsh (shell) + Powerlevel0k [source](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k)
```bash
pacman -S zsh
# Configuration de base :
zsh /usr/share/zsh/functions/Newuser/zsh-newuser-install -f

# Installation du plugin
yay -S zsh-theme-powerlevel10k-git
echo 'source /usr/share/zsh-theme-powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc

# Définir zsh comme shell par défaut :
chsh
/bin/zsh
reboot

# Quelques alias
alias ls='ls --color=auto' # coloration des dir
alias maj='sudo pacman -Syu'
alias aur='yay -Syu --aur'
alias bye='sudo shutdown now'
alias clean='yay -Sc'
alias zshmaj='source ~/.zshrc'
alias error='systemctl --failed && echo ------------ && journalctl -p 3 -xb'
alias mirror='sh ~/Scripts/maj_mirrors' # Voir script-reflector.md

# Binkeys
bindkey "^[[3~" delete-char
```

