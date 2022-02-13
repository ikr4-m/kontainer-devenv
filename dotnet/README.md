How to run this image manually:
```sh
docker build -t image:tags . && \
    docker run --volume /static/path/to/workdir:/app/workdir \
    --name container_name \
    -dit image:tags
```
