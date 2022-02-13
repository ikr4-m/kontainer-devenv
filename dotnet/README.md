# .NET Core
Running in .NET Core 6.0 with Ubuntu Focal

## How To Run
- Manually
```sh
docker build -t netcore:latest . && \
    docker run --volume /static/path/to/workdir:/app/workdir \
    --name container_name \
    -d netcore:latest
```
- Using compose
```sh
docker compose up
```
