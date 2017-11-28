# nt_docker
[![N](https://www.novatec-gmbh.de/fileadmin/styles/novatec_v5.5/images/header-logo.jpg)](https://www.novatec-gmbh.de/)

## Containers

 Service | Address 
 --- | ---
 Jenkins | http://localhost:8001
 GitLab | http://localhost:8002
 MongoDB | http://localhost:8003


## Start Containers

To start the containers:
1. Make sure Docker is running
`sudo systemctl start docker`
2. Switch to the nt_docker folder
`cd /usr/docker/nt_docker`
3. And run the containers (in Background mode) with
`docker compose up -d`
4. Wait 3-5 minutes

To stop the containers simply run the command `docker-compose stop`
