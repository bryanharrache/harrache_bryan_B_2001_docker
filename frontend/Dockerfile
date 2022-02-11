# Image de base
FROM node:8.11-alpine

#Copie de la liste des dependance 
COPY package.json /app/package.json

#Installation des dependances
RUN cd /app && npm install 

# Copie du code applicatif
COPY . /app

# Répertoire de travail de l'application
WORKDIR /app

# Port d'écoute
EXPOSE 3000

#Commande à lancer
CMD ["npm", "start"]
