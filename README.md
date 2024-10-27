# DEPI (DevOps) -Project

Hello All,

This repo is for a DevOps project with the below segmentation for the project :

Idea :

- Is to automate a CI/CD pipeline to host an application on AWS EKS using the below tools and technologies :

  1- Source Control: GitHub to store the code and for version control for the app and the needed yaml files.
  2- CI/CD Pipleline: Jenkins to automate the build and deployment process.
  3- Configuration managment: Ansible to configure the Jenkins worker node which is hosted on AWS EC2.
  4- Containerization: Docker to build the application.
  5- Artifact Repository: Docker Hub to store our images.
  6- EKSCTL: To create the needed resources on AWS EKS where the application will be deployed through yaml file.
  7- Orchestration: Kubernetes for the deployment, load balancer and auto scaling group.
  8- Slack: Using slack to notify if the pipeline succeed or failed.

  Project Flow :

  Step 1: Developers to push the application code on GitHub.
  Step 2: Create an AWS EC2 to be worker node for Jenkins.
  Step 3: Configure the EC2 using ansible to pass the needed dependiencies.
  Step 4: To start the Jenkins pipeline where the main pipeline and yaml files are stored on GitHub repo.
  Step 5: The pipeline will build the app an push it to docker hub repo, AWS EKS resources will be created using EKSCTL and kubernetes wll be deployed on the created resources.
  Step 6: From the output of Jenkins we can get the public DNS to access the deployed app.
