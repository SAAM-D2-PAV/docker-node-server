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


#### Pour lancer un sevice en particulier
```console
    docker compose -f docker-compose.dev.yml run le_nom_du_service

    ex : docker compose -f docker-compose.dev.yml run db
 ```
#### Initialiser la bdd
```console
   docker compose -f docker-compose.dev.yml run db
   docker container exec -it ID mongosh
   use test
   db.count.insertOne({count: 0})
   exit

 ```


 ### étape 01 - build les environnements de dev et de tests
```console
 docker compose -f docker-compose.dev.yml up --build
 ```