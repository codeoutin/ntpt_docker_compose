# NTPT Docker Compose

This is a Docker Compose file, which installs a Code Environment Server.
Current the following containers are included
* [Jenkins CI Server](https://hub.docker.com/r/stegerpa/jenkins/)
* GitLab Server
* MongoDB Database
* SonarQube Quality Gate

## Containers
 Service | Address 
 --- | ---
 Jenkins | http://localhost:8001
 GitLab | http://localhost:8002
 MongoDB | http://localhost:8003
 SonarQube | http://localhost:8004

## Install
1. Type command `mkdir /usr/docker && cd /usr/docker` to create the directory, where we store the yaml file
2. Clone the file by using command `git clone https://github.com/stegerpa/nt_docker.git && cd nt_docker`
3. Make sure to install [Docker Compose](https://github.com/docker/compose/releases) before continuing

## Start Containers
To start the containers:
1. Make sure Docker is running
`sudo systemctl start docker`
2. Switch to the nt_docker folder
`cd /usr/docker/nt_docker`
3. And run the containers (in Background mode) with
`docker-compose up -d`
4. Wait 3-5 minutes

To stop the containers simply run the command `docker-compose stop`
