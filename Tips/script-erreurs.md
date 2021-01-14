## Script pour vérifier les erreurs système

* Création du script
```bash
touch check_errors # Création du fichier
nano check_errors # Edition du fichier
```

* Script
```bash
#!/bin/sh
#Vérification des erreurs
sudo systemctl --failed
sudo journalctl -p 3 -xb
```

* Exécution du script
```bash
chmod +x check_errors # Rendre le script executable
./check_errors # Exécution du script