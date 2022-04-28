List all volumes

```{bash}
$ docker volume ls
```

Create new volume

```{bash}
$ docker volume create example-volume
```

Mount new volume to container to folder /misko

```{bash}
docker run -d --rm --name container2 --mount source=example-volume,target=/misko alpine tail -f /dev/null
```

Get details about volume 
```{bash}
docker volume inspect example-volume
```
