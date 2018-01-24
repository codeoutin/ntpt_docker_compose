# Customized Jenkins

This Jenkins Image is build on [jenkins:alpine](https://hub.docker.com/_/jenkins/). The Image is hosted in [Docker Hub](https://hub.docker.com/r/stegerpa/jenkins/)
Modifications made:
* Install Plugins
* Disable Security
* Setup Admin User
  * username: admin / password: admin


## Build

To build and push the image use
* Build: `docker image build -t stegerpa/jenkins .`
* Push: `docker image push stegerpa/jenkins`
