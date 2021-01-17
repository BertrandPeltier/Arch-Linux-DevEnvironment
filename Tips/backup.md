## Script pour faire un backup d'un dossier

* Création du script
```bash
touch backup # Création du fichier
nano backup # Edition du fichier
```

* Script
```bash
#!/bin/sh
#Compression et backup du dossier user >> sf_VM_SHARE
tar -czvf backup-`date +%Y-%m-%d-%H-%M`.tar.gz ~/'folder' # Ajout de la date + heure au nom du fichier
mv backup-`date +%Y-%m-%d-%H-%M`.tar.gz /media/sf_VM_SHARE/ # Copie vers le dossier partagé
```

* Exécution du script
```bash
chmod +x backup # Rendre le script executable
./backup # Exécution du script