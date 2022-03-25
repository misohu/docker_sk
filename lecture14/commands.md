Create postgres and pgadmin volumes (not necessary but for completeness)
```{bash}
$ docker volume create postgres
$ docker volume create pgadmin
```

Create Postgrsql container in new netwrok
```{bash}
docker run --rm --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d --net psql -v pgdata:/var/lib/postgresql/data postgres
```

Create pgadmin container and expose to port 80 in new network
```{bash}
$ docker run -p 80:80 --rm -d -e 'PGADMIN_DEFAULT_EMAIL=user@domain.com' -e 'PGADMIN_DEFAULT_PASSWORD=SuperSecret' --net psql -v pgadata:/var/lib/pgadmin dpage/pgadmin4
```

```{bash}
$ docker run --rm -p 8000:8000 --net psql --mount type=bind,source="$(pwd)/school_project,target=/app" school-rest:1
```