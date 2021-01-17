## Activation de numlock au boot de la console

* Création du fichier script :
```bash
touch /usr/local/bin/numlock
```

* Script
```bash
#!/bin/bash

for tty in /dev/tty{1..6}
do
    /usr/bin/setleds -D +num < "$tty";
done
```

* Rendre exécutable le script
```bash
chmod +x /usr/local/bin/numlock
```

* Création du service
```bash
touch /etc/systemd/system/numlock.service`
```

* Code du service
```bash
[Unit]
Description=numlock

[Service]
ExecStart=/usr/local/bin/numlock
StandardInput=tty
RemainAfterExit=yes

[Install]
WantedBy=multi-user.target
```

* Activation du service
```bash
systemctl enable numlock.service`
reboot
```