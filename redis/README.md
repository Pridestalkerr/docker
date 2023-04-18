## Setup

This docker compose file uses the bitnami/redis image. It runs as non root by default, so you're gonna have to change the permissions of the cache folder to allow the redis user to write to it.

```
mkdir cache
sudo chown -R 1001:1001 cache
```

## Persistence

The docker compose file mounts a volume for the cache folder. This means that the data will persist even if the container is destroyed.
