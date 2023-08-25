
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

Create a `codebuild` project in aws and give the `path to buildspec file from your repo`.

-------------------------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------------------------

![image](https://github.com/Glenrodrigues/CiCD-using-ECS-and-docker-/blob/main/images/Screenshot%202023-08-25%20162638.png)


### Note: change the black box data according to your region an ECR repo URI 



### Explanation
* Before pre build we define our app environmet 'node js' and `activate docker demon to build docker image`
* #### Pre Build:
    * Get AWS version
    * AWS region 'us-east-2'
    * login in to AWS ECR
    * COMMIT hash
    * Creating image tag
* #### Build:
   * Building `Docker-image`.
   * Tagging the Image.
* #### Post Build:
   * Push the image to ECR repo.
   * creating Artifact
* ### Artifact:
   * Artifcat name.json
     Artifact will store in S3 bucket.






