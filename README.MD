### Step 1 - Construire l'image
```console
 docker build -t nom_de_l_image .
 ```

### Vérifier le container
```console
docker image ls
 ```

### Step 2 - Lancer le container sur l'image
```console
docker run -it -p 3000:3000 --name nom_de_l_image nom_du_container
 ```

 ### Step 3 - Lancer le container en live reload
 ```console
docker run --name --rm nom_du_container -p  3000:3000 --mount type=bind,src="$(pwd)"/app,target=/app --mount type=volume,target=/app/node_modules nom_de_l_image
 ```
### exemple
  ```console
docker run --rm --name nodereactapplr -p 3000:3000 --mount type=bind,src="$(pwd)"/app,target=/app --mount type=volume,target=/app/node_modules nodereactapp
 ```