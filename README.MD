## Installation et configuration 

### étape 00 (si update de react)
```console

 npx create-react-app app
 supprimer le dossier app/node_modules
 cd app/
 touch Dockerfile.dev

 ```
```console

FROM node:alpine
WORKDIR /app
COPY package.json .
RUN npm install
COPY . .
CMD ["npm", "start"]

 ```
 ### étape 01 - build les environnements de dev et de tests
```console
 docker compose -f docker-compose.dev.yml up --build
 ```