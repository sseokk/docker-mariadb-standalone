# docker-mariadb-standalone

Docker Compose - MariaDB Standalone


# .ENV
```
MARIADB_ROOT_PASSWORD=rootpasswd
MARIADB_DATABASE=dev
MARIADB_USER=dev
MARIADB_PASSWORD=devpasswd
```

# Customize - docker-compose.yml
```yml
...
ports:
      - "42306:3306"
...
command:
      - --character-set-server=utf8mb4
      - --collation-server=utf8mb4_unicode_ci
```

# How to Use ?

## Run
```bash
$ docker compose up
```
Or with Daemon
```bash
$ docker compose up -d
```

## init Seed
```
./sql/1-seed.sql
./sql/2-seed.sql
./sql/3-seed.sql
./sql/4-seed.sql
```

# Down
```bash
$ docker compose down
```

# Cleanup DB Volume
```bash
$ docker compose down
$ sh ./clean-data.sh
```