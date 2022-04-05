# Minikube deployment of a flask app, using docker. #

source code repository : https://github.com/singularityltd/minikube_hello_world

dockerhub location : docker pull singularityltd/singularity-flask-webapp:latest

This piece of work assumes you have a fully functioning minikube.

Steps to build :

1. cd into the docker directory,  and follow the build instructions within README.md

Following  a successful docker build..

2. cd into the minikube_config and once again follow the instructions within README.md

Once configured the flask webapp will be loadbalanced within minikube,   and the webapp
can be accessed on the url within the README.md.   The IP will be assigned by minikube,  
so its important to check for the IP as documented.

