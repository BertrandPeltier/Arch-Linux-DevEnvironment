## Installation de Git + paramétrage

* Installation de Git
```bash
pacman -S git
```

* Configuration locale de Git
```bash

git config --global user.name 'user' # Le nom qui apparaîtra sur les commit

git config --global user.email 'email' # L'email associé au commit

git config --global core.editor code # Choix de l'éditeur, ici VSC

git config --global color.ui true # Activation des couleurs dans le résultat des commandes Git

git config -l # Pour vérifier toutes les infos
```

* Création d'une clé SSH pour GitHub
```bash
ssh-keygen -t rsa -b 4096 -C 'email' # Création de la clé

cat ~/.ssh/id_rsa.pub # Récupérer le contenu de notre clé publique
```

**Sur GitHub :**
Settings > SSH and GPG keys > New SSH key > Coller le contenu de la clé et valider

* Activation de la clé SSH en local
```bash
eval "$(ssh-agent -s)" # pour lancer ssh-agent de façon sécurisée
ssh-add ~/.ssh/id_rsa # pour activer la clé SSH
```

