# Customized Jenkins

This Jenkins Image is build on jenkins:alpine.
Modifications made:
* Install Plugins
* Disable Security
* Setup Admin User
  * username: admin / password: admin


## Build

To build the image use
`docker image build -t stegerpa/jenkins .`
`docker image push stegerpa/jenkins`