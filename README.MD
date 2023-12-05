### Construire l'image
```console
 docker build -t myapp .
 ```

### Lancer un conteneur sur l'image
```console
docker run -it myapp sh
```

### Lancer un container avec retour terminal host

```console 
docker run -d --name appnode -p 80:80 myapp
```

### Puis récupérer le terminal du container

```console 
docker exec -it appnode sh
```

### Stats et charge d'utilisation

```console 
docker container stats appnode
```


### Port host: port container

```console
docker run -p 8081:80 myapp
```

### Kill apahe sur l'host

```console 
sudo apachectl stop
```
