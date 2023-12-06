
### Construire et/ou lancer le container avec persistance de donnée et ouverture du shell
```console
docker run --mount type=bind,source="$(pwd)"/data,target=/data -it alpine sh
 ```

 ### Vérifier le container
```console
 ls
 ```