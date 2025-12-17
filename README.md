# Docker Images for Local Development & Testing

This repository contains a collection of reusable Docker images focused on
local development, testing, and quick environment setup.

The main goal is to simplify running common stacks and tools without polluting
the host machine, while keeping environments as close as possible to real
production scenarios.

---

## Why this repository exists

In many real-world projects, setting up local environments becomes slow,
inconsistent, and error-prone — especially when switching between different
languages, frameworks, and infrastructure stacks.

This repository was created to:

- Speed up local environment setup
- Standardize development and testing environments
- Avoid installing heavy dependencies directly on the host OS
- Provide disposable containers for debugging and connectivity tests
- Improve developer productivity and reduce onboarding friction

---

## Quick Start

All services will be available on their respective ports once the containers
are up and running.
Start the entire local development stack using Docker Compose:

```bash
docker compose up -d
```

To stop and remove all containers created by Docker Compose:

```bash
docker compose down
```

---

## Available Images, Access URLs & Default Credentials

> ⚠️ All credentials listed below are intended for local development only.

- **RabbitMQ (3.x with Management UI)**  
  - **Management UI:** http://localhost:15672  
  - **AMQP Port:** `5672`
  - **Username:** `guest`  
  - **Password:** `guest`

- **PostgreSQL 13**
  - **Host:** `localhost`
  - **Port:** `5435`
  - **Database:** `postgres`
  - **Username:** `root`
  - **Password:** `root`

- **MySQL 8.4**
  - **Host:** `localhost`
  - **Port:** `3306`
  - **Database:** `default`
  - **Username:** `root`
  - **Password:** `root`

- **MongoDB Community Server**
  - **Host:** `localhost`
  - **Port:** `27017`
  - **Authentication Database:** `admin`
  - **Username:** `root`
  - **Password:** `root`

- **Redis 7.2**
  - **Host:** `localhost`
  - **Port:** `6379`
  - **Authentication:** Not enabled (local development)

- **Redis Commander**
  - **Management UI:** http://localhost:8081  

- **Elasticsearch 8.8**
  - **HTTP API:** http://localhost:9200
  - **Transport Port:** `9300`
  - **Security:** Disabled (local development)

- **Kibana 8.8**
  - **Web UI:** http://localhost:5601
  - **Elasticsearch Host:** http://elastic:9200

---

## Author

Henrique von Weidebach