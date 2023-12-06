### Construire l'image
```console
 docker build -t myapp .
 ```

### Vérifier le container
```console
docker image ls
 ```

### Lancer le container
```console
docker run --name react -p 3000:3000 myreact
 ```