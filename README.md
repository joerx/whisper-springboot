# Whisper Backend

A considerate microblogging-api built with Springboot. Backend application.

## Setup

- Make Postgres run
- Create a new database
- Import [schema.sql](./src/main/resources/schema.sql)

## Configuration

```sh
DATASOURCE_URL=jdbc:postgresql://postgres:5432/whisper
DATASOURCE_USERNAME=postgres
DATASOURCE_PASSWORD=postgres
SERVER_PORT=9090
```

## Docker

- `dockerfile-maven-plugin` doesn't seem to play nicely with newer Docker versions on macos
- Since [docker-client](https://github.com/spotify/docker-client) is inactive, this looks unlikely to be fixed
- Using a simple Makefile instead:

```sh
# Build
make clean docker-build

# Push
make clean docker-push
```

## API Usage

See [docs/api.md](./docs/api.md)
