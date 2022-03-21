Create Postgrsql container
```{bash}
docker run --rm --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d  postgres
```

Create pgadmin container and expose to port 80
```{bash}
$ docker run -p 80:80 --rm -d -e 'PGADMIN_DEFAULT_EMAIL=user@domain.com' -e 'PGADMIN_DEFAULT_PASSWORD=SuperSecret' dpage/pgadmin4
```

Check for container ip 
```{bash}
$ docker inspect <container_id>
```
