# Database Collection
List database provider:
- MariaDB
- Redis
- Mongo

## Setup
1. Setup all the password in the `.env`.

## How To Run
```sh
# Activate development environment
docker compose up -d

# Login to database (MariaDB)
mariadb -h 127.0.0.1 -u mariadb -p

# Login to database (Redis)
redis-cli -h 127.0.0.1 --pass redisdb

# Login to database (Mongo)
mongo --host 127.0.0.1:27017 --username mongodbroot --password mongodb

# Deactive development environment
docker compose down
```
