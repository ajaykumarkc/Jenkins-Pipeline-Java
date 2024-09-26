# Jenkins Pipeline for Java based application using Maven, SonarQube, Argo CD and Kubernetes

![CI_CD drawio](https://github.com/user-attachments/assets/977138db-11b9-4c05-8faf-528cc463cac8)


Here are the step-by-step details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD, and Kubernetes:

Prerequisites:

   -  Java application code hosted on a Git repository
   -  Jenkins server
   -  Kubernetes cluster
   -  Helm package manager
   -  EC2 Instance (t2 large and above)
   -  Argo CD

Steps:

    1. Install the necessary Jenkins plugins:
       1.1 Git plugin
       1.2 Maven Integration plugin
       1.3 Pipeline plugin
       1.4 Kubernetes Continuous Deploy plugin
       1.5 Docker Plugin
       1.6 Sonar Plugin

    2. Create a new Jenkins pipeline:
       2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.
       2.2 Add a Jenkinsfile to the Git repository to define the pipeline stages.

    3. Define the pipeline stages:
        Stage 1: Checkout the source code from Git.
        Stage 2: Build the Java application using Maven.
        Stage 3: Run SonarQube analysis to check the code quality.
        Stage 4: Package the application into a JAR file.
        Stage 5: Promote the application to a production environment using Argo CD.

    4. Configure Jenkins pipeline stages:
        Stage 1: Use the Git plugin to check out the source code from the Git repository.
        Stage 2: Use the Maven Integration plugin to build the Java application.
        Stage 3: Use the SonarQube plugin to analyze the code quality of the Java application.
        Stage 4: Use the Maven Integration plugin to package the application into a JAR file.
        Stage 5: Use the Kubernetes Continuous Deploy plugin to deploy the application to a test environment using Helm.
        Stage 6: Use Argo CD to promote the application to a production environment.

    5. Set up Argo CD:
        Install Argo CD on the minikube cluster and port forward and add your repo paths.
        Set up a Git repository for Argo CD to track the changes in the deployment.yml in the manifests.

    6. Run the Jenkins pipeline:
       7.1 Trigger the Jenkins pipeline to start the CI process for the Java application.
       7.2 Monitor the pipeline stages and fix any issues that arise.

This end-to-end Jenkins pipeline will automate the entire CI/CD process for a Java application, from code checkout to production deployment, using popular tools like SonarQube, Argo CD and Kubernetes.

# Images

## Build Success
![Build Success](https://github.com/user-attachments/assets/3fb707a0-45fb-4cef-9e8f-6205477df227)

## sonar qube testing
![sonar qube testing](https://github.com/user-attachments/assets/7998a98d-a02f-49f0-a2e9-61ffcb0110bd)

## deployments on minikube cluster using argocd
![deployments on minikube cluster using argocd](https://github.com/user-attachments/assets/0d14fc6f-c45f-402b-a37a-abf6e04578ec)
