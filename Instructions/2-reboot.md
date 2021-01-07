## First reboot

* Ajouter un utilisateur + passwd
```bash
useradd -m -g users -G wheel -s /bin/bash 'username'
passwd 'username'
```

* Attribution des droits `sudo`
```bash
pacman -S sudo # Instaalation du paquet sudo
EDITOR=nano visudo # Edition des privilèges
# Puis décommenter la ligne
'%wheel ALL=(ALL) ALL'
# Cette ligne pour supprimer le recours au passwd (si besoin)
'%wheel ALL=(ALL) NOPASSWD=ALL'
```

* Vérification des erreurs
```bash
systemctl --failed
journalctl -p 3 -xb
```

* Exemple d'erreur
```bash
`dhcpcd[248] no valid interfaces found` # google it
```