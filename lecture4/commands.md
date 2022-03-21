List images in local repository

```{bash}
$ docker image ls
```

Build Docker image named **ubuntu-test** from Dockerfile located at current directory (must be named Dockerfile)

```{bash}
$ docker build -t ubuntu-test .
```

Build Docker image named **ubuntu-test** from Dockerfile located at path

```{bash}
$ docker build -t ubuntu-test -f /path/to/DifferentDockerfileName .
```

Run image as container (must be presented in local registry). Random Name will be generated

```{bash}
$ docker run ubuntu-test
```

Run image as container (must be presented in local registry). Specify name

```{bash}
$ docker run --name ubuntu-test-container ubuntu-test
```

List running containers

```{bash}
$ docker ps
```

List all containers

```{bash}
$ docker ps --all
```

Remove container

```{bash}
$ docker rm <container_id_or_name>
```

Remove image. !!! You cannot simply remove image which container is used (exited state)

```{bash}
$ docker image rm <image_id>
```

Stop running container

```{bash}
$ docker stop <container id or name>
```
