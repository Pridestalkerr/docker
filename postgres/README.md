## Setup

This docker compose file uses the bitnami/postgresql image. It runs as non root by default, so you're gonna have to change the permissions of the pgdata folder to allow the postgresql user to write to it.

```
mkdir pgdata
sudo chown -R 1001:1001 pgdata
```

## Persistence

The docker compose file mounts a volume for the pgdata folder. This means that the data will persist even if the container is destroyed.
