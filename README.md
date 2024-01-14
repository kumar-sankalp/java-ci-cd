# Java Spring Boot CI/CD Pipeline

This project sets up a CI/CD pipeline for a Java Spring Boot application using Jenkins and ArgoCD, deployed on Kubernetes using the GitOps approach.

**Check out the detailed documentation by clicking on this link:**  https://devops-maestro.gitbook.io/cicd-pipeline-using-jenkins-and-argocd/

## Features

1. **Automated Triggers**: Any code changes pushed to the repository automatically trigger the build process in Jenkins using a Docker agent.
2. **Build Process**: The code is cloned from the repository and Maven builds an archive.
3. **Static Code Analysis**: SonarQube performs static code analysis to check for any code vulnerabilities.
4. **Docker Image Creation**: A Docker image is built from the Maven archive and pushed to DockerHub.
5. **Automated Manifest Updates**: Shell scripts automatically update the Docker image tag in the deployment manifest files.
6. **Deployment**: ArgoCD picks up the changes in the manifests repository and creates an application, which ultimately deploys the Spring application to the Kubernetes cluster.

## Prerequisites

- Jenkins
- ArgoCD
- Docker
- Kubernetes
- SonarQube
- Maven
