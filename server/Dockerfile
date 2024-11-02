# Utiliser l'image de base Node.js (Alpine pour une image plus légère)
FROM node:lts-alpine

# Définir le répertoire de travail à l'intérieur du conteneur
WORKDIR /app

# Copier les fichiers package.json et package-lock.json
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier le reste des fichiers du serveur
COPY . .

# Exposer le port 5001
EXPOSE 5001

# Démarrer l'application avec npm
CMD ["npm", "start"]


