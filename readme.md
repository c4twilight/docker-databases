# Docker Databases Toolkit

Production-style local database setup using Docker Compose for backend development.

## Included Databases
- MySQL (+ Adminer)
- PostgreSQL (+ Adminer)
- MongoDB
- Redis (+ RedisInsight)

Learning comments are kept in compose/readme files and organized for clarity.

## Prerequisites
- Docker Desktop or Docker Engine with Compose plugin

## Environment Variables
1. Copy `.env.example` to `.env`
2. Update credentials as needed

## Quick Start
From repository root, run one stack at a time:

```bash
docker compose -f ./mysql/docker-compose.yml up -d
docker compose -f ./postgresql/docker-compose.yml up -d
docker compose -f ./mongodb/docker-compose.yml up -d
docker compose -f ./redis/docker-compose.yml up -d
```

## Health Checks
- MySQL: `mysqladmin ping`
- PostgreSQL: `pg_isready`
- MongoDB: `db.adminCommand('ping')`
- Redis: `redis-cli ping`

## Stop Stack
```bash
docker compose -f ./mysql/docker-compose.yml down
docker compose -f ./postgresql/docker-compose.yml down
docker compose -f ./mongodb/docker-compose.yml down
docker compose -f ./redis/docker-compose.yml down
```

## Ports
- MySQL: `3306`
- PostgreSQL: `5432`
- MongoDB: `27017`
- Redis: `6379`
- Adminer: `8080`
- RedisInsight: `8001`
