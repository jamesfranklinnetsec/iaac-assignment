# find it working online here
http://ec2co-ecsel-39dby778rhnl-557674916.us-west-2.elb.amazonaws.com:8080/hello

# About project:
# Create AWS Account and deploy a:
* Hello World Java Application ([Spring Boot framework](https://start.spring.io/)) 
	- ~~I'm using [this tutorial](https://www.youtube.com/watch?v=vtPkZShrvXQ) to get my hello world going~~
	- done. check the demo folder for the hello world.
* Running as a container
	- ~~using [this tutorial](https://spring.io/blog/2018/11/08/spring-boot-in-a-container)~~
	- now using [this](https://stackoverflow.com/questions/27767264/how-to-dockerize-maven-project-and-how-many-ways-to-accomplish-it) instead as it seems more appropriate.
* Using a container orchestration of your choice
	- ~~the spring boot tutorial recommends docker, so docker it is.~~
	- dockerise -> put into pod -> deploy to k8s
* Exposed via a LoadBalancer
	- I'll probably use nginx
	-- find an nginx k8s tutorial
# Bonus:
* Automated Pipelines for Deployment
* All AWS Infrastructure is deployed as script
	- probably via tf. I don't have time to go learn cloudformation just yet.



# build container:

* cd into demo
	- ./makedocker to make the container image and stick it into ECR
# running:

* tbd on infra
* to run locally
	- cd back out into root dir. of project and ./cmdtorun.sh
	- navigate to http://localhost:8080/hello
	- should say 'hello world' if it isn't bugging out. last build I made seems to bug out and I'm not sure what to do to fix it so I'm just going to move on to infrastructure stuff for now.
