
## Setup

### Postgres

For local development the postgres db will be hosted inside a docker container:
    
    ```bash
    docker pull postgres
    ```
        
    ```bash
    docker run --name postgres -e POSTGRES_PASSWORD=postgres -d -p 5432:5432 postgres
    ```
    
This creates a fresh postgres instance with username and password `postgres` and exposes the port `5432` to the host machine.

The database can be accessed with the following command:

    ```bash
    docker exec -it postgres psql -U postgres
    ```
