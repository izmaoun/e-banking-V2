FROM node:20-alpine AS build
WORKDIR /app

# Copier les fichiers de dépendances
COPY package*.json ./
RUN npm install

# Copier tout le code
COPY . .

# Exposer le port
EXPOSE 4200

# Démarrer Angular avec host 0.0.0.0 pour Docker
CMD ["npm", "start", "--", "--host", "0.0.0.0"]
