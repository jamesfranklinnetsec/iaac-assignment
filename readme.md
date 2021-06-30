# find it working online here
http://ec2co-ecsel-39dby778rhnl-557674916.us-west-2.elb.amazonaws.com:8080/hello
![Screenshot from 2021-06-30 12-36-49](https://user-images.githubusercontent.com/57028307/123893540-e6caa600-d99f-11eb-9d68-cd8f74cd78d2.png)


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
	- ~~dockerise -> put into pod -> deploy to k8s~~
	- dockerise -> stick into ECR -> deploy with ECS
* Exposed via a LoadBalancer
	- ~~I'll probably use nginx~~
	-- ~~find an nginx k8s tutorial~~
	- ECS has a button for "do you want a load balancer with that?". I will be going with the no-code philosophy :--)
# Bonus:
* Automated Pipelines for Deployment
* All AWS Infrastructure is deployed as script
	- probably via tf. I don't have time to go learn cloudformation just yet.

    dockerise -> stick into ECR -> deploy with ECS

Exposed via a LoadBalancer

    I'll probably use nginx -- find an nginx k8s tutorial

# build container:

* cd into demo
	- ./makedocker to make the container image and stick it into ECR
# running:

* on AWS infra
	- get the [AWS CLI tool](https://aws.amazon.com/cli/) and authenticate to the relevant zone with [this guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html#cli-configure-quickstart-creds). You need this to stick your container onto AWS ECR.
	- to stick your container onto ECR, go [here](https://us-west-2.console.aws.amazon.com/ecr/get-started?region=us-west-2). Make a public repo, and give it a name. Mine ended up being public.ecr.aws/z4k2y4o4/hello-world-spring.
	- run docker login 
	- 
* to run locally
	- cd back out into root dir. of project and ./cmdtorun.sh
	- navigate to http://localhost:8080/hello
	- should say 'hello world' if it isn't bugging out. last build I made seems to bug out and I'm not sure what to do to fix it so I'm just going to move on to infrastructure stuff for now.
