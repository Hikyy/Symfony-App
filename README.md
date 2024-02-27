# App Symfony Dockerisée

## Description

Ceci est un exemple de projet Symfony dockerisé, configuré pour être accessible sur `localhost:8080`. 

L'application utilise Docker et Docker Compose pour faciliter le déploiement et la gestion des dépendances.

## Techno utilisées

- [Symfony](https://symfony.com/): Un framework PHP robuste pour le développement web.
- [Docker](https://www.docker.com/): Une plateforme open-source pour automatiser le déploiement d'applications dans des conteneurs.
- [Nginx](https://www.nginx.com/): Un serveur web léger et rapide, utilisé ici comme serveur HTTP.
- [MariaDB](https://mariadb.org/): Un système de gestion de base de données relationnelles.
- [Adminer](https://www.adminer.org/): Un outil de gestion de base de données, accessible sur [http://localhost:8080](http://localhost:8080).


## Prérequis

Assurez-vous d'avoir installé les outils suivants sur votre machine avant de commencer :

- Docker
- Docker Compose

## Prérequis

La base du squelette symfony a été construit en suivant la documentation de symfony.

Je vous renvoie vers celle-ci : [Symfony Skeleton](https://symfony.com/doc/current/setup.html)

## Installation

1. Clonez le repository :

   ```bash
   git clone git@github.com:Hikyy/Symfony-App.git
   ```
    ```bash
    cd Symfony-App
    ```

2. Construisez et démarrez les conteneurs Docker :

    ```bash
    docker compose up -d --build
    ```

3. Installez les dépendances Symfony en accédant au conteneur PHP :

    ```bash
    docker compose exec php composer install
    ```

4. Lancez le serveur Symfony :
  
    ```bash
      docker compose exec php symfony serve --allow-http
    ```

5. Pour accéder à la page de démarrage de Symfony :

    ```bash
      localhost:8000
    ```
