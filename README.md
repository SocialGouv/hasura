# Hasura

Hasura service for *Carnets* application.

## Run locally

Build the container:
```shell
docker build -t hasura .
```

Create a `.env` file containing the following information:
```shell
HASURA_GRAPHQL_DATABASE_URL=postgres://postgres:postgrespassword@postgres:5432/postgres
HASURA_GRAPHQL_ADMIN_SECRET=myadminsecretkey
HASURA_GRAPHQL_ENABLE_CONSOLE=true
HASURA_GRAPHQL_ENABLED_LOG_TYPES=startup, http-log, webhook-log, websocket-log, query-log
```

Run the container:
```shell
docker run -it --rm -p 8080:8080 --env-file=.env hasura
```
