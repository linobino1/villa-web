# villa-web

Plain html website + listmonk newsletter system.

## Services
### web

plain html website

### Newsletter System

listmonk with PostgreSQL database

## Setup Dev Environment

start listmonks database:
```
docker compose -f docker-compose.ymal -f docker-compose.development.yaml up -d listmonk_db
```

initialize listmonks database:
```
docker compose -f docker-compose.yaml -f docker-compose.development.yaml run --rm listmonk ./listmonk --install
```

start all services:
```
docker compose -f docker-compose.ymal -f docker-compose.development.yaml up -d
```

## Deployment

create network 'net' using `docker network create net`

start listmonks database:
```
docker compose -f docker-compose.yaml -f docker-compose.production.yaml up -d listmonk_db
```

initialize listmonks database:
```
docker compose -f docker-compose.yaml -f docker-compose.production.yaml run --rm listmonk ./listmonk --install
```

start all services:
```
docker compose -f docker-compose.yaml -f docker-compose.production.yaml up -d
```