# Docker Compose Repository

Welcome to the Docker Compose Repository! This repository serves as a collection of Docker Compose files for various services, making it easy to set up and manage different containers.

## Table of Contents

- [PostgreSQL and pgAdmin](#postgresql-and-pgadmin)
  - [Description](#description)
  - [Usage](#usage)
  - [Environment Variables](#environment-variables)

---

## PostgreSQL and pgAdmin

### Description

The Docker Compose file (`docker-compose-postgres.yml`) in this section sets up a PostgreSQL database server (version 14.1) along with pgAdmin4, providing a convenient environment for database management.

### Usage

To start the services, run the following command:

```bash
docker-compose -p postgres -f docker-compose-postgres.yml up -d
```

To build the images and start the services:

```bash
docker-compose -p postgres -f docker-compose-postgres.yml up -d --build
```

#### PostgreSQL

The PostgreSQL server is accessible on localhost:5432. You can connect using the specified username and password.

#### pgAdmin

The pgAdmin interface is accessible on localhost:8080 [localhost:8080](http://localhost:8080). Use the specified email address and password to log in.

### Environment Variables

- **PostgreSQL Service (postgres)**

  - **POSTGRES_HOST_AUTH_METHOD**: Specifies the authentication method for the PostgreSQL server. In this example, it is set to "trust" for simplicity.
  - **POSTGRES_PASSWORD**: The password for the PostgreSQL user.
  - **POSTGRES_USER**: The username for the PostgreSQL user.

- **pgAdmin Service (pgadmin)**
  - **POSTGRES_HOST_AUTH_METHOD**: Specifies the authentication method for connecting to the PostgreSQL server. In this example, it is set to "trust" for simplicity.
  - **PGADMIN_DEFAULT_EMAIL**: The default email address for the pgAdmin user.
  - **PGADMIN_DEFAULT_PASSWORD**: The default password for the pgAdmin user.
