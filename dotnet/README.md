# .NET Core
Running in .NET Core 6.0 with Ubuntu Focal

## Setup
1. Set UID and GID user that you want code it into `.env`.

Get UID: `sudo id -u <username>`

Get GID: `sudo id -g <username>`

3. If you want to use dotnet tools, modify `DOTNET_TOOLS` in `.env`.

## How To Run
- Manually
```sh
# Build image and run it
docker build -t netcore:latest . && \
    docker run --volume /static/path/to/workdir:/app/workdir \
    --name container_name \
    -d netcore:latest
```

- Using compose
```sh
# Activate development environment
docker compose up --build -d && docker compose exec dotnet bash

# Deactive development environment
docker compose down
```

## Notes
- This container using single env file, just modify one source .env file in this file.
- **Don't delete env file with `DOTNET_` prefix.**
