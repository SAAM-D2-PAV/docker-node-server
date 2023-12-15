### Construire l'image et lancer le container
```console
 docker compose up --build
 ```

### ou
```console
docker compose up
 ```

### Serveur de tests

#### Step 1 - récupérer l'id du container de test
```console
docker container ls
 ```

 #### Step 2 - attacher le second terminal
```console
docker container attach NOM_OU_ID
 ```

 ### Couper proprement 
 ```console
docker compose down -v
 ```

 ### Interaction cli avec le serveur de test
 ```console
 -> docker container ls
 -> docker attach ID / nom du container
 -> ex docker attach 24866fddc722

 Watch Usage
 › Press f to quit "only failed tests" mode.
 › Press o to only run tests related to changed files.
 › Press q to quit watch mode.
 › Press i to run failing tests interactively.
 › Press p to filter by a filename regex pattern.
 › Press t to filter by a test name regex pattern.
 › Press Enter to trigger a test run.
 ```

 ### Environnement de prod sur nginx 
 ```console
docker compose -f docker-compose.prod.yml up
 ```
