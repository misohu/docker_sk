Connect folder to container (bind mount)

```{bash}
$ docker run -p 8888:8888 --name jupyter --rm --mount type=bind,source="$(pwd)",target=/app jupyter:1
```