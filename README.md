# Store Service

A Kotlin + Spring Boot microservice for store operations. 
This guide walks you through setting up a PostgreSQL database using Docker and getting the application running locally.

---

## Getting Started

### Prerequisites

- Java 21+
- Maven
- Docker

---

## Running PostgreSQL with Docker

To avoid needing a full PostgreSQL install, run it using Docker.

### 1. Start the PostgreSQL Container

```bash
docker run --name store-postgres \
  -e POSTGRES_USER=storeuser \
  -e POSTGRES_PASSWORD=storepass \
  -e POSTGRES_DB=storedb \
  -p 5432:5432 \
  -d postgres:16