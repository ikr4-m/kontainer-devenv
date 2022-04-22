# If you want to customize like volumes path, min-max usage, env file, networks, etc,
# I suggest you modified the compose than this Dockerfile.

# Import Dotnet SDKs
FROM mcr.microsoft.com/dotnet/sdk:6.0-focal
LABEL name "Dotnet Core DevEnv"

# Set workdir
WORKDIR /app/workdir

# Make group, and add user based on UID & GID
ARG UID=1000
ARG GID=1000
RUN groupadd -g $GID dotnet && useradd dotnet -m -u $UID -g $GID
USER dotnet

# If the tool is not available from .env, don't install
ARG DOTNET_TOOLS=""
RUN if [ "$DOTNET_TOOLS" = "" ] ; then echo "Skipping installing Dotnet tools." ; else dotnet tool install $DOTNET_TOOLS -g ; fi

# Stall the process
ENTRYPOINT ["tail", "-f", "/dev/null"]
