# Utiliser l'image de base Node.js
FROM node:18-alpine

# Définir le répertoire de travail à l'intérieur du conteneur
WORKDIR /app

# Copier les fichiers package.json et package-lock.json
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier les autres fichiers du client
COPY . .

# Construire l'application React
RUN npm run build

# Installer un serveur HTTP léger pour servir les fichiers statiques de l'application
RUN npm install -g serve

# Exposer le port 3000
EXPOSE 3000

# Démarrer l'application en mode production
CMD ["serve", "-s", "build"]

