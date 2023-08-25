
# CI/CD Pipeline for AWS ECS


### Note: I have a basic project of music webapp , i will be using ECS and docker to deploy it on cloud. 

`Amazon Elastic Container Service (ECS)` is Amazon’s solution for running and orchestrating Docker containers. It provides an interface for defining and deploying Docker containers to run on clusters of EC2 instances or Farget.

### Prerequisites
* You should have VPC created in your account with Public and Private Subnets and Private subnets should have a route to NAT Gateway.

* Amazon Elastic Container Service (ECS) Cluster.

* Application Load Balancer.

* ECR Repository.

* Permission to Create IAM roles, policies.

* 'Buildspec file' to build project. 

* 'Docker' file to containerized application.


## Lets get started

Step 1

Push you code to `AWS codecommit` (you code should also have docker and buildspec file) .

Step 2 

Create a `codebuild` project in aws and give the `path to buildspec file from your repo` .



