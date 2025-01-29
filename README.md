# RideOrCry - Running with Docker Compose

This guide provides instructions to set up and run the RideOrCry application using Docker Compose.

## Prerequisites
- [Docker](https://docs.docker.com/get-docker/) installed on your machine.
- [Docker Compose](https://docs.docker.com/compose/install/) installed.

## Download the Repository
Clone the repository to your local machine:
```sh
git clone https://github.com/ihopewecanchangeitlater/Cloud-Services-Development
cd Cloud-Services-Development
```

## Start the Application
To start the application using Docker Compose, run:
```sh
docker-compose up --build -d
```
This will start two containers:
1. **PostgreSQL Database** (RideOrCry-DB)
2. **Spring Boot Application** (RideOrCry-SERVER)
3. **React.js served on nginx** (RideOrCry-CLIENT)

## Access the Application
Once the containers are running, access the application at:
```
http://localhost:3000
```

## Stop the Application
To stop the running containers, use:
```sh
docker-compose down
```

## Clean Up
To remove the containers and associated volumes:
```sh
docker-compose down -v
```

## Troubleshooting
- Ensure ports 8080 and 5432 are available on your machine.
- Run `docker compose logs` to check logs if the application fails to start.

---
Developed with ❤️ by RideOrCry Team
