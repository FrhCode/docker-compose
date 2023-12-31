# PostgreSQL and pgAdmin Docker Setup

This repository contains a Docker Compose configuration for setting up PostgreSQL and pgAdmin containers.

## Prerequisites

- [Docker Installation](https://docs.docker.com/engine/install/)
- [Docker Compose Installation](https://docs.docker.com/compose/install/)

## Getting Started

1. **Clone this repository:**

   ```bash
   git clone https://github.com/FrhCode/docker-compose cd docker-compose
   ```

2. **Adjust the configuration (if needed):**

   Open **docker-compose-postgres.yml** and modify environment variables, such as passwords or email addresses, according to your preferences.

3. **Build and start the containers:**

   ```bash
   docker-compose -p postgres -f docker-compose-postgres.yml up -d --build
   ```

4. **Access pgAdmin:**

   - Open your browser and go to http://localhost:8080.
   - Log in with the email and password specified in the docker-compose-postgres.yml file.

5. **Connect to PostgreSQL:**

   Use pgAdmin to connect to the PostgreSQL database using the provided credentials.

## Environment Variables

- **PostgreSQL Service (postgres)**

  - **POSTGRES_HOST_AUTH_METHOD**: Specifies the authentication method for the PostgreSQL server. In this example, it is set to "trust" for simplicity.
  - **POSTGRES_PASSWORD**: The password for the PostgreSQL user.
  - **POSTGRES_USER**: The username for the PostgreSQL user.

- **PgAdmin Service (pgadmin)**
  - **POSTGRES_HOST_AUTH_METHOD**: Specifies the authentication method for connecting to the PostgreSQL server. In this example, it is set to "trust" for simplicity.
  - **PGADMIN_DEFAULT_EMAIL**: The default email address for the pgAdmin user.
  - **PGADMIN_DEFAULT_PASSWORD**: The default password for the pgAdmin user.
