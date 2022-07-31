# Déployer WordPress avec Docker

## Cloner le dépôt

```
git clone https://github.com/cpuch/docker-wordpress
```

## Renommer et éditer le fichier .env.sample

```
cd docker-wordpress
mv .env/sample .env
```

Par exemple :

```
# Docker Compose
COMPOSE_PROJECT_NAME=my_project

# MariaDB
MARIADB_DATABASE=wordpress
MARIADB_ROOT_PASSWORD=r00tme
MARIADB_USER=wordpress
MARIADB_PASSWORD=changeme

# WordPress
# /!\ Ne pas change la variable WORDPRESS_DB_HOST /!\ 
WORDPRESS_DB_HOST=db
WORDPRESS_DB_NAME=wordpress
WORDPRESS_DB_USER=wordpress
WORDPRESS_DB_PASSWORD=changeme
```

## Démarrer la stack

```
docker compose up -d
```

## Terminer l'installation de WordPress

Ouvrir un navigateur à http://localhost:8000
