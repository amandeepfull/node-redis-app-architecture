
branches:
1. new_contact_app :  configurations for running multi-container app using docker-compose in local environment
2. multi-container-EB: configuration for deploying app to AWS elastic Beanstalk
3. kubernetes: configurations for running kubernetes in minikube(local environment)
4. k8s/production: configurations to deploy Google Cloud Kubernetes Engine

# Contact App

Its Contact application app, where we can store our contacts with few more information

In this project we learned :
1. create architecture for node app and database as Redis cache
2. Frontend is in react.js
3. Docker and Kubernetes

# Stack used:
1. Node.js
2. Redis
3. React.js
4. Redux.js
5. Docker
6. Kubernetes
7. Google Cloud 
8. Travis CI: Continous deployment and integration

Redis : we configure for only local host, if we want we can directly connect with remote host of redis server and make use.

if we are using google cloud platform and want to use redis we can use in following ways:
1. create a VM under compute engine.
2. Install redis on VM and using internal Ip of VM we can connect to redis server.

if we want to manage remote redis from our local we can link remote server with our local machine using external Ip of specific VM machine.
It will make the things easy for debugging and we can configure all things by our localhost.

# To Start Project in Mac
1. Download docker in your machine
2. Run Docker in your machine.
3. Go to app directory
4. docker-compose up --build 

# Docker terminal commands:
1.  docker run image

2.  docker ps 

3.  docker ps -all

4.  docker build .

5.  docker build -t <user-name>/<project-name>:1.0.0 // we can specify version as tag for image

6.  docker run -p osExternalPort:imagePortSpecified image 

7.  docker images

8.  docker start containerId

9.  docker start -i containerId

10. docker stop containerId

11. docker kill containerId

12. docker logs

13. docker exec -it containerId <image specific command>: we will just go inside the container and write image specific commands, for eg: Image is redis, docker run -it redis redis-cli. we will go right into redis cli to manage redis in container.

14. docker exec -it containerId sh:

15. docker build -f <Docker File Name> . :  building docker with different filename

16. docker build -f <file-url> -t <uname>/<app-name> .
# Docker Compose terminal commands
1. docker-compose build .

2. docker-compose up

3. docker-compose stop

4. docker-compose start

5. docker-compose kill

6. docker-compose logs

# Docker Volume
How to use in React App:
1. Run react app using docker-compose up
2. Open another terminal and enter command npm run watch

Now if we make any changes in app and reload the browser it can reflect in browser.

#K8S Setup
1. Install Orace VirtualBox : It works as virtual machine on our local machine.
1. Install minikube : It is a tool which run K8s locally on the virtual machine
2. Install kubectl : It consist of commands which can be use locally and in production to manage kubernetes


# Commands
1. Deleting webhook configuration : kubectl delete validatingwebhookconfiguration ingress-nginx-admission
 

 # Logging architecture with Kubernetes
 1. Fluentd : Log aggregator 
 https://docs.fluentd.org/v/0.12/articles/kubernetes-fluentd
 
 2. ElasticSearch: storage/search
 3. Kibana: UI
**Learning and building is in under process**

