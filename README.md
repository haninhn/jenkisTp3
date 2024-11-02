# MERN APP

## Vue d'Ensemble
Ce projet est une application full-stack qui consiste en un client React et un serveur Node.js utilisant MongoDB comme base de données. Docker est utilisé pour la conteneurisation, et Docker Compose est utilisé pour orchestrer les services.

## Table des Matières
- [Technologies Utilisées](#technologies-utilisées)
- [Variables d'Environnement](#variables-denvironnement)
- [Configuration de Docker](#configuration-de-docker)
- [Images Docker](#images-docker)
- [Docker Compose](#docker-compose)
- [Comment Exécuter le Projet](#comment-executer-le-projet)

## Technologies Utilisées
- **Frontend** : React
- **Backend** : Node.js, Express
- **Base de Données** : MongoDB
- **Conteneurisation** : Docker, Docker Compose

## Variables d'Environnement
Les variables d'environnement suivantes sont utilisées dans l'application :

- **REACT_APP_API_URL** : Cette variable contient l'URL de base pour le serveur API. Elle est utilisée dans le client React pour faire des requêtes au serveur.
- **MONGO_URI** : L'URI de connexion à MongoDB utilisée par le serveur pour se connecter à l'instance MongoDB.

## Configuration de Docker
Ce projet comprend des Dockerfiles pour le client et le serveur, qui facilitent la construction et l'exécution des services dans des conteneurs isolés. Les configurations incluent :

- **Client** : Un environnement Node.js pour construire l'application React. Les dépendances sont installées et l'application est construite pour une utilisation en production. Un serveur HTTP simple peut être utilisé pour servir l'application construite.
  
- **Serveur** : Un environnement Node.js qui installe les dépendances nécessaires et configure l'application pour écouter sur un port spécifique.

## Images Docker
Les images Docker créées pour ce projet sont les suivantes :

- **Image du Client** : `node:lts-alpine`
- **Image du Serveur** : `node:lts-alpine`
- **Image de la Base de Données** : `mongo:latest`

Ces images sont spécifiées dans les Dockerfiles respectifs et sont utilisées lors de la construction et du déploiement des services.

## Docker Compose
Docker Compose est utilisé pour gérer les différents services de l'application, y compris le client, le serveur et MongoDB. Les services sont interconnectés, ce qui permet une communication fluide entre le client et le serveur. Le fichier de configuration spécifie les images, les ports exposés, ainsi que les variables d'environnement nécessaires pour chaque service.

## Comment Exécuter le Projet
1. Assurez-vous d'avoir Docker et Docker Compose installés sur votre machine.
2. Clonez ce dépôt sur votre machine locale.
3. Accédez au répertoire du projet dans votre terminal.
4. Construisez et démarrez l'application en utilisant Docker Compose :

   ```bash
   docker-compose up --build
   ```

5. Accédez au client à [http://localhost:3000](http://localhost:3000).

## docker set up 
1 Créer les Dockerfiles
   Dockerfile pour le client (front)
   Dockerfile pour le serveur(back)
   Construiser  l'image Docker pour le serveur et le client 
      ```bash

     docker build -t mern-client .
     docker build -t serveur .
      ```
2 Créer un réseau Docker 
      ```bash
   docker network create mern-network
      ```
3 Exécuter MongoDB dans un conteneur
      ```bash
  docker run -d --name mongodb --network mern-network mongo
         ```

4 Exécuter les conteneurs du serveur et du client
    ```bash
    docker run -d --name server --network mern-network -p 5001:5000 mern-server
    docker run -d --name client --network mern-network -p 3000:3000 mern-client
    ```
5 Créer un fichier Docker Compose
6 Lancer l'application avec Docker Compose
  ```bash
  docker-compose up --build
   ```

 ** Docker va créer un container pour chaque partie :**

Un container pour React (client).
Un container pour Express (server).
Un container pour MongoDB (base de données).


Docker Compose orchestre ces trois containers pour qu'ils communiquent entre eux comme une seule application. Tu définis les instructions dans un fichier docker-compose.yml, et Docker Compose va tout gérer à ta place : démarrer, arrêter, construire et relier les containers.

dockerfile : creation d un Dockerfile pour chaque partie de  l'application (client et serveur) qui décrit comment construire le container.
Docker Compose : Dans le fichier docker-compose.yml, definire les services (client, serveur, MongoDB) pour qu'ils s'exécutent ensemble.

## Exécution des commandes Docker :
docker build : Construit une image Docker à partir du Dockerfile.
docker run : Démarre un container à partir de l'image Docker construite.
docker-compose up --build : Construit et démarre tous les containers définis dans le fichier Docker Compose.
