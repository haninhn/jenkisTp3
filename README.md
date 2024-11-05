##Documentation TP2: Déploiement d'une application MERN avec Docker et Docker Compose
introduction:
Ce projet vise à containeriser une application MERN (MongoDB, Express, React, Node.js) et à orchestrer les différents conteneurs avec Docker Compose. Il s'agit d'une application web composée 
d'un client React et d'une API Express connectée à une base de données MongoDB.

Pré-requis:

Instalation de Docker.
Instalation de Docker Compose.
    
## Docker Compose
Docker Compose est utilisé pour gérer les différents services de l'application, y compris le client, le serveur et MongoDB. Les services sont interconnectés, ce qui permet une communication fluide entre le client et le serveur. Le fichier de configuration spécifie les images, les ports exposés, ainsi que les variables d'environnement nécessaires pour chaque service.


1. Cloner le projet
Clonez le dépôt GitLab contenant l'application MERN :
  ```bash 
    git clone https://gitlab.com/devops_tps/mern-app
    cd mern-app 
   ```

 2.Création des Dockerfiles     

 Dockerfiles pour le client et le serveur: 
 facilitent la construction et l'exécution des services dans des conteneurs isolés. Les configurations incluent :


- **Client** : Un environnement Node.js pour construire l'application React. Les dépendances sont installées et l'application est construite pour une utilisation en production. Un serveur HTTP simple peut être utilisé pour servir l'application construite.
  
- **Serveur** : Un environnement Node.js qui installe les dépendances nécessaires et configure l'application pour écouter sur un port spécifique.
 
   Dockerfile pour le client (front)
   Dockerfile pour le serveur(back)
  
 3. Construiser  l'image Docker pour le serveur et le client
  ## Images Docker
Les images Docker créées pour ce projet sont les suivantes :

- **Image du Client** : `node:14-alpine`
- **Image du Serveur** : `node:14-alpine`
- **Image de la Base de Données** : `mongo:latest`

Ces images sont spécifiées dans les Dockerfiles respectifs et sont utilisées lors de la construction et du déploiement des services.
      ```bash 
      
     docker build -t mern-client .
     docker build -t serveur .
      ```
2 Créer un réseau Docker 
Pour permettre la communication entre les conteneurs, créez un réseau Docker :


      ```bash
      
     docker network create mern-network
      ```
3 Exécuter MongoDB dans un conteneur
 ** Docker va créer un container pour chaque partie :**
  
  Un container pour React (client).
  Un container pour Express (server).
  Un container pour MongoDB (base de données).

      ```bash
      
       docker run -d --name mongodb --network mern-network mongo
        ```

4 Exécuter les conteneurs du serveur et du client
    ```bash
    
    docker run -d --name server --network mern-network -p 5001:5000 mern-server
    docker run -d --name client --network mern-network -p 3000:3000 mern-client
    ```
5 Créer un fichier Docker Compose
   Dans le répertoire racine du projet, créer un fichier docker-compose.yml pour orchestrer les trois services : MongoDB, serveur, et client
   
6 Lancer l'application avec Docker Compose
Pour lancer l'application avec Docker Compose, utilisez la commande suivante :

  ```bash
  docker-compose up --build
   ```

## Exécution des commandes Docker :
docker build : Construit une image Docker à partir du Dockerfile.
docker run : Démarre un container à partir de l'image Docker construite.
docker-compose up --build : Construit et démarre tous les containers définis dans le fichier Docker Compose.
