# Jenkins Pipeline for DevOps Project

This repository contains a Jenkins pipeline script designed to automate various stages of a DevOps project. The pipeline is configured to clean the workspace, clone a Git repository, check Docker container status, and perform SonarQube code analysis.

## Jenkinsfile

The `Jenkinsfile` in this repository defines the Jenkins pipeline. It consists of several stages:

### 1. Clean Folder

This stage cleans the Jenkins workspace to ensure a fresh environment for the pipeline execution. It then prints the current working directory and clones the specified Git repository using the provided URL.

### 2. SonarQube Analysis

This stage of the pipeline performs a code analysis using SonarQube. It assumes that SonarQube is configured as a tool in Jenkins and named 'sonar'. The SonarQube scanner is invoked to analyze the code, providing the project key as a parameter.

## Running the Pipeline

To run this pipeline in Jenkins, follow these steps:

1. Install Jenkins on your server or use an existing Jenkins instance.
2. Create a new pipeline project in Jenkins.
3. Configure the pipeline to use the `Jenkinsfile` from this repository.
4. Define the necessary parameters, such as the Git URL.
5. Run the pipeline and monitor the execution in the Jenkins dashboard.

## Prerequisites

Before running this pipeline, ensure the following:

- Jenkins is installed and configured properly.
- Docker is installed on the Jenkins agent or node.
- SonarQube is configured as a tool in Jenkins with the name 'sonar'.
- Access to the specified Git repository.

## Author

Arkyy
