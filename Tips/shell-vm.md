## Script pour le shell de VM

Ce script permet de régler le problème de démarrage de la VM

* Création du fichier script
```bash
fs0:
edit startup.nsh
```

* Script

```bash
fs0:
cd efi
cd boot
bootx64.efi
```

Puis F2 (save) et F3 (exit)

![Détail des commande shell](./img/startup-nsh-cmd.PNG)

```bash
reset
```