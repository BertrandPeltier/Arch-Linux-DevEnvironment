## Mise à jour du système & pacman

[Source](https://wiki.archlinux.org/index.php/pacman)

* Mise à jour du système
```bash
pacman -Syu # Synchronisation et mise à jour des paquets
```

* Gestion des paquets
```bash
pacman -S 'paquet' # Installation d'un paquet

pacman -Rs 'paquet' # Désinstallation du paquet + ses dépendances qui ne plus requises par aucun autre paquet

pacman -Qi 'paquet' # Recherche d'un paquet parmi ceux installés

pacman -Si 'paquet' # Recherche d'un paquet dans les dépôts
```

* Nettoyage du système
```bash
pacman -Sc # supprime tous les paquets non-installés du cache (anciennes versions ou non installées sur le système)
```