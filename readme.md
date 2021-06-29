# Create AWS Account and deploy a:
* Hello World Java Application ([Spring Boot framework](https://start.spring.io/)) 
	- I'm using [this tutorial](https://www.youtube.com/watch?v=vtPkZShrvXQ) to get my hello world going
	- done. check the demo folder for the hello world.
* Running as a container
	- ~~using [this tutorial](https://spring.io/blog/2018/11/08/spring-boot-in-a-container)~~
	- now using [this](https://stackoverflow.com/questions/27767264/how-to-dockerize-maven-project-and-how-many-ways-to-accomplish-it) instead as it seems more appropriate.
* Using a container orchestration of your choice
	- the spring boot tutorial recommends docker, so docker it is.
* Exposed via a LoadBalancer
	- I'll probably use nginx
# Bonus:
* Automated Pipelines for Deployment
* All AWS Infrastructure is deployed as script
	- probably via tf. I don't have time to go learn cloudformation just yet.
