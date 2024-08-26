# Verwende ein Node.js-Image als Basis
FROM node:14-alpine

# Setze das Arbeitsverzeichnis im Container
WORKDIR /app

# Kopiere package.json und installiere Abhängigkeiten
COPY package*.json ./
RUN npm install

# Kopiere den restlichen Code in das Arbeitsverzeichnis
COPY . .

# Erzeuge die Produktions-Builds, falls notwendig
RUN npm run build

# Exponiere den Port, auf dem die Anwendung läuft
EXPOSE 3000

# Starte die Anwendung
CMD ["npm", "start"]