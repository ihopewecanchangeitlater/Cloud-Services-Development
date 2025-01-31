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
git submodule init
git submodule update
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

## Update Submodules
To update submodules to latest changes, run:
```sh
git submodule update --remote
git add .
git commit -m "git submodule updated"
git push origin
```

## Troubleshooting
- Ensure ports 8080 and 5432 are available on your machine.
- Run `docker compose logs` to check logs if the application fails to start.

## Video
[Ride or Cry](https://youtu.be/-YudLKLcTu0)

---
Developed with ❤️ by RideOrCry Team
