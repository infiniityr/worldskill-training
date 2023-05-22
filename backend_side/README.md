# Backend

## Setup

Pour mettre en place l'env de développement, lancer les commandes suivantes :

### Linux

```bash
sudo apt install apache2 php8.1
sudo cp ./sources/backend_site.conf /etc/apache2/sites-enabled/
sudo a2enmod vhost_alias rewrite
sudo systemctl start apache2
```

### Macos

```bash
brew install httpd php@8.1
sudo cp ./sources/backend_site.conf /etc/httpd/sites-enabled/
sudo a2enmod vhost_alias rewrite
sudo brew services start httpd
```

Mettre à jour le fichier `backend_site.conf` copier pour remplacer `/path/to` par le chemin vers le dossier `worldskill-training`.
Redémarrer le serveur web avec la commande `sudo systemctl restart apache2` (Linux) ou `sudo brew services start httpd` (MacOS).

Modifier ensuite le fichier `/etc/hosts`, utiliser pour ça la commande `sudo nano /etc/hosts` (ou `vim`)
Ajouter les lignes suivantes.

```text
127.0.0.1 back.worldskill.local exercice1.back.worldskill.local
```
