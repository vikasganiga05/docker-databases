# Docker Databases Toolkit

Run database services locally with Docker. This repository is intended to keep
the container configuration and instructions needed to start and manage those
services in one place.

## Requirements

- Docker Desktop or Docker Engine with Compose plugin.

## Included Databases

- MySQL (+ Adminer)
- PostgreSQL (+ Adminer)
- MongoDB
- Redis (+ RedisInsight)

## Usage

From the repository root, start the services defined by the Compose
configuration:

```sh
docker compose up -d
```

Check running services and follow their logs:

```sh
docker compose ps
docker compose logs -f
```

Stop the services:

```sh
docker compose down
```

To remove the services and their persisted volumes (which deletes stored
database data), run `docker compose down --volumes`.

## Configuration

Set database credentials, ports, and other options in the applicable Compose
configuration or environment file. Keep secrets out of version control; use
local environment files and provide a safe example file for shared settings.
