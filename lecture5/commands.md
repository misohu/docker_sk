Build jupyter lab image with tag custom-jupyter:1

```{bash}
$ docker build -t custom-jupyter:1 .
```

Run the image with port mapped

```{bash}
$ docker run --rm -p 8888:8888 -d custom-jupyter:1
```
