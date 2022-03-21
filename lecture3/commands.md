Get docker version
```{bash}
$ docker --version
```

List images in local repository
```{bash}
$ docker image ls 
```

List running containers 
```{bash}
$ docker ps 
```

List all containers (including exited)
```{bash}
$ docker ps --all 
```

Run Wordpress container locally with custom name 
```{bash}
$ docker run --rm --name michals-wordpress -p 80:80 wordpress
```
