# Java Spring Boot CI/CD Pipeline using Jenkins & ArgoCD

**Check out the detailed documentation by clicking on this link:**  https://devops-maestro.gitbook.io/cicd-pipeline-using-jenkins-and-argocd/

![diagram-export-21-1-2024-5_29_21-pm](https://github.com/devops-maestro17/java-cicd-pipeline/assets/148553140/ecfc670b-10e6-429c-a61d-85736771cafc)


Welcome to the GitOps-centric CI/CD pipeline designed for deploying Java Spring Boot applications on Kubernetes, utilizing Jenkins as the Continuous Integration (CI) tool and Argo CD as the Continuous Deployment (CD) tool. This comprehensive pipeline ensures a seamless and automated deployment process. Let's delve into the project's key steps:

## Step 1: GitHub Webhook Initiates Jenkins Build
- Automatic triggers are set up through GitHub webhooks, initiating the Jenkins build process upon any code changes.
- Jenkins responds promptly, ensuring the pipeline stays agile and responsive to real-time updates.

## Step 2: Maven Build for Java Application
- Jenkins clones the code from the repository and employs Maven to build an application archive.
- The Maven build process ensures a streamlined and efficient compilation of the Java Spring Boot application.

## Step 3: Static Code Analysis with SonarQube
- Emphasizing code quality and security, SonarQube is integrated for static code analysis.
- Vulnerabilities are identified, ensuring a clean and secure codebase for the application.

## Step 4: Dockerization and Image Tagging on DockerHub
- The Maven archive undergoes Dockerization to encapsulate the application in a Docker image.
- DockerHub serves as the centralized repository where the Docker image is pushed and versioned.
- This structured versioning process ensures clarity in managing application releases.

## Step 5: Update Deployment Manifests Using Shell Scripts
- Shell scripts seamlessly integrate the tagged Docker image into deployment manifests.
- This update triggers Argo CD to pick up the changes, facilitating the deployment of the latest application version.

## Step 6: Continuous Deployment with Argo CD in GitOps Fashion
- Argo CD continually monitors the manifests repository housing deployment and service manifests.
- Upon detecting changes, Argo CD orchestrates the deployment to the Kubernetes cluster.
- This aligns with the GitOps paradigm, defining the desired state in Git for consistent infrastructure and application management.

## Conclusion
This GitOps-centric CI/CD pipeline, powered by Jenkins and Argo CD, automates and streamlines the deployment of Java Spring Boot applications on Kubernetes. The integration of Docker, SonarQube, and versioning practices ensures a comprehensive and secure software delivery lifecycle. Explore the future of DevOps with GitOps!

### Technologies Used:
- Jenkins
- Argo CD
- Docker
- Kubernetes
- Maven
- SonarQube
