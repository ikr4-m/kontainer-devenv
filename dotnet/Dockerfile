# If you want to customize like volumes path, min-max usage, env file, networks, etc,
# I suggest you modified the compose than this Dockerfile.

# Btw, if you want to run it manually, just type this command below
# docker build -t image:tags . && \
#   docker run --volume /static/path/to/workdir:/app/workdir \
#   --name container_name -dit image:tags

# Import Dotnet SDKs
FROM mcr.microsoft.com/dotnet/sdk:6.0-focal
LABEL name "Dotnet Core DevEnv"

# Set workdir
WORKDIR /app/workdir

# If you want to add some tools from dotnet, insert here
#RUN dotnet tool install dotnetsay
