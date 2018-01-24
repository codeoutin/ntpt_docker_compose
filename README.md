# NTPT Docker Compose

This is a Docker Compose file, which setup a Prototype Environment for developers. Its part of NTPT, so you probably also want to use
* [NTPT Frontend](https://github.com/stegerpa/ntpt_frontend_react)
* [NTPT Backend (Server)](https://github.com/stegerpa/ntpt_camunda_server)

Current the following containers are included
* [Customized Jenkins CI Server](https://hub.docker.com/r/stegerpa/jenkins/)
* [GitLab CE Server](https://hub.docker.com/r/gitlab/gitlab-ce/)
* [MongoDB Database](https://hub.docker.com/_/mongo/)
* [SonarQube Server](https://hub.docker.com/_/sonarqube/)
* [Sherpa Docker API](https://hub.docker.com/r/djenriquez/sherpa/)

## Containers
 Service | Address | Description
 --- | --- | ---
 Custom Jenkins | http://localhost:8001 | Default Login: admin::admin, Security Disabled
 GitLab | http://localhost:8002 | Create User at first Start
 MongoDB | http://localhost:8003 | Security disabled
 SonarQube | http://localhost:8004 | Default Login: admin::admin
 Docker API | http://localhost:4550 | Security disabled

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

## Alternatives to GitLab
This Project is created as part of my Bachelor Thesis. Since GitLab needs a lot of memory and CPU power to run, you could also try out some Alternative Git Services:
* [Gogs.io](https://gogs.io/)
* [GitBucket](https://github.com/gitbucket/gitbucket)
* [Gitolite](http://gitolite.com/gitolite/)
