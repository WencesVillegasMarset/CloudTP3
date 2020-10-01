# TP3 Cloud Computing - 2020 | Wenceslao Villegas

### Para correr el ejemplo ejecutar:

```console
bash:~$ docker network create awslocal # creamos red
bash:~$ docker run -p 8000:8000 --network awslocal --name dynamodb dwmkerr/dynamodb -sharedDb # Base de datos
bash:~$ sam local start-api --docker-network awslocal # Lambda
```

El setup de la Base de Datos se realiza ejecutando el codigo setup_db.js en la shell de Dynamo (i.e localhost:8000/shell)