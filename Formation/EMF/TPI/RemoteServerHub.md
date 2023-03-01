# RemoteServerHub

  

## Description

RemoteServerHub est une application web de gestion de compte SSH. Elle vous offre la possibilité de vous connecter à distance à vos serveurs en utilisant une interface web. Elle est conçue pour être facile à utiliser et comprend des fonctionnalités avancées pour gérer efficacement vos serveurs distants.

## But de l’application

Le but de l’application est principalement d’avoir une seul interface qui permet de géré tous les identifiants des serveurs pour se connecter en ssh ou en ftp dans un deuxième temps.

## Les technologies utilisé :

- Docker

- HTML CSS JS

- PHP Symfony

- MariaDB

### Docker

Pour facilité le déploiement de l’application, docker permet de créer un image de cet application qui sera par la suite accessible depuis le navigateur.

### HTML CSS JS

Pour le frontend, une interface faite avec bootstrap sera utilisé.

### PHP

PHP permet de faire la communication avec les serveurs ainsi que la base de données pour récupérer les identifiants importé ou enregistré précédemment.

### MariaDB

Pour stocker les identifiants des serveurs, ils se trouveront dans une base de données.

## Objectif de base :

- [ ] Ajouter un enregistrement de serveur

- [ ] Pouvoir se connecter à se serveur et exécuter des commandes

- [ ] Pouvoir importer et exporter les hosts

- [ ] Avoir des groups/catégories d’hosts (Exemple : Priver, Travail,…)


## Idée secondaire

- [ ] Pouvoir importer des hosts appartir d’export de autre application (Filezila,…)

- [ ] Pouvoir se connecter en FTP et faire du CRUD

- [ ] Avoir accès à terminal local

- [ ] Un système de snippet (Commande pré-enregistrer)

- [ ] Faire du “monitoring” (?)

- [ ] Ouvrir plusieur terminal

- [ ] Trouver un moyen pour faire de la sychronisation de compte (?)


## Test téchnologique a faire :

- [ ] Créer une image docker avec une application react, un serveur php et une db (TT_docker)

- [ ] Interconnecter React et php (TT_React-PHP)

- [ ] Faire une connexion en php à un serveur (TT_SSH)
  

### TT_docker

Pour ce test, j’ai essayé de créer une image docker de rien. En premier lieu, il a fallut créer un Dockerfile. Voici un exemple de la structure du document :

```docker

# Base image

FROM node:14 AS node

  

# Set workdir

WORKDIR /app

  

# Copy the React app

COPY ./app /app

  

# Install dependencies

RUN npm install

  

# Build the React app

RUN npm run build

  

# Base image

FROM php:8.0-apache

  

# Copy the built React app

COPY --from=node /app/build /var/www/html

COPY /app/backend /var/www/html/backend

  

# Install PHP extensions

RUN docker-php-ext-install pdo_mysql

  

# Start Apache

CMD ["apache2-foreground"]

```

Puis j’ai du créer aussi une docker-compose.yaml pour faire un container de cet image :

```bash

version: '3'

services:

web:

build: .

ports:

- "80:80"

db:

image: mariadb:10.5

environment:

MYSQL_ROOT_PASSWORD: password

MYSQL_DATABASE: database

MYSQL_USER: user

MYSQL_PASSWORD: password

```

Pour démarrer cet image, suffit d’executer cet commande :

```bash

# Permet de créer l'image

docker-compose build

  

# Permet d'executé l'image

docker-compose up -d

```

Maintenant, l’application web est accéssible depuis `http://localhost:80`
  
### TT_SSH

docker-compose.yaml

```bash

version: '3.8'

services:

php-apache-environment:

container_name: php-apache

build: ./

volumes:

- .:/var/www/html/

ports:

- 8080:80

```

Dockerfile

```bash

FROM php:8.0-apache

  

RUN apt-get update

RUN apt-get install -y libssh2-1 libssl-dev gcc make wget

  

RUN mkdir tmp

RUN cd tmp

RUN wget https://libssh2.org/download/libssh2-1.10.0.tar.gz

RUN tar vxzf libssh2-1.10.0.tar.gz

RUN cd libssh2-1.10.0/

RUN ./configure

RUN make

RUN make install

  

RUN pecl install ssh2-1.3.1

  

RUN echo "extension=ssh2.so" > /usr/local/etc/php/conf.d/ssh2.ini

```

Problème actuel:

- Installation de l’extension ssh2 pour faire des requêtes ssh au serveur

Solution:

- Faire une configuration personnalisé de docker en installant les dépendances nécéssaires pour faire fonctionner ssh2 à traver le dockerfile

- Source : [https://ao-system.net/en/note/194](https://ao-system.net/en/note/194)

### Se connecter à un serveur en ssh depuis php:

```php

$connection = ssh2_connect($srv, $port);

  

if (ssh2_auth_password($connection, 'usr', 'pwd')) {

echo "Authentication Successful!\n";

} else {

die('Authentication Failed...');

}

```

## Commande utile


| docker exec -it cbf4ad73bf85 /bin/bash | Permet de se connecter en ssh à un container |

| --- | --- |

| docker ps | lister les containers |

| docker container kill $(docker container ls -q) | Shutdown tout les containers |

  

## Test à effectuer avant de rendre le projet

  

- [ ] Wireshark lors de la connexion pour voir s’il y a pas le mdp qui passe en clair