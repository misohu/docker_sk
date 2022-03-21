List docker networks 
```{bash}
docker network ls
```

Create new custom bridge network
```{bash}
docker network create psql
```

Create Postgrsql container in new netwrok
```{bash}
docker run --rm --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d --net psql  postgres
```

Create pgadmin container and expose to port 80 in new network
```{bash}
$ docker run -p 80:80 --rm -d -e 'PGADMIN_DEFAULT_EMAIL=user@domain.com' -e 'PGADMIN_DEFAULT_PASSWORD=SuperSecret' --net psql dpage/pgadmin4
```

Check containers in network 
```{bash}
$ docker network inspect <network_id>
```
