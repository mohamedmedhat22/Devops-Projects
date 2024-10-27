# DevOps Project: CI/CD Pipeline on AWS EKS

Welcome! This repository is for a DevOps project focused on building and automating a CI/CD pipeline to deploy an application on AWS EKS. Below is an outline of the tools, technologies, and project flow.

---

## Project Idea

The aim of this project is to automate a CI/CD pipeline using the following tools and technologies:

- **Source Control**: GitHub - for storing code and managing version control for the app and YAML files.
- **CI/CD Pipeline**: Jenkins - automates the build and deployment process.
- **Configuration Management**: Ansible - configures the Jenkins worker node hosted on AWS EC2.
- **Containerization**: Docker - builds the application into a container.
- **Artifact Repository**: Docker Hub - stores application images.
- **EKSCTL**: Provisions resources on AWS EKS, where the application is deployed using YAML configuration.
- **Orchestration**: Kubernetes - manages deployment, load balancing, and auto-scaling of the application.
- **Notifications**: Slack - sends notifications on pipeline success or failure.

---

## Project Workflow

1. **Code Push**  
   Developers push application code to GitHub, triggering the CI/CD pipeline.

2. **Setup Jenkins Worker**  
   An AWS EC2 instance is provisioned to serve as the Jenkins worker node.

3. **Configuration with Ansible**  
   The EC2 instance is configured with necessary dependencies using Ansible.

4. **Pipeline Execution**  
   The Jenkins pipeline is executed, with the pipeline and YAML files stored in this GitHub repository.

5. **Build and Deployment**  
   - The pipeline builds the application and pushes it to Docker Hub.
   - Resources on AWS EKS are created using EKSCTL.
   - Kubernetes deploys the application on the provisioned resources.

6. **Access the Application**  
   The public DNS output from Jenkins allows access to the deployed application.

---

Thank you for checking out this project! Feel free to explore the repository and reach out if you have any questions.
