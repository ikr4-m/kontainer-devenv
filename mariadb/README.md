MariaDB Database in Container.

## Setup
1. Setup all the password in the `.env`.

## How To Run
```sh
# Activate development environment
docker compose up -d

# Login to database (MariaDB)
mariadb -h 127.0.0.1 -u mariadb -p

# Deactive development environment
docker compose down
```
