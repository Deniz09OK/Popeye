# Utilisation de Node.js version 21 basée sur Alpine
FROM node:21-alpine  
# Définition du répertoire de travail de docker
WORKDIR /app  
# Copie du fichier package.json pour installer les dépendances
COPY package.json ./  
# Installation des dépendances sans les packages inutiles pour la production
RUN npm install --only=production  
# Copie du reste des fichiers de l'application
COPY . .  
# Exposition du port 80 pour l'application Node.js
EXPOSE 80  
# Commande pour démarrer le serveur Node.js
CMD ["node", "server.js"]