# Jenkins Pipeline for CI/CD with Docker and SonarQube Integration

This repository contains a Jenkins pipeline script (`Jenkinsfile`) for setting up a Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins, Docker, and SonarQube.

## Prerequisites
- Jenkins server installed and configured
- Docker installed on the Jenkins server
- SonarQube server installed and configured

## Jenkins Pipeline Configuration
The Jenkins pipeline script (`Jenkinsfile`) defines the following stages:

1. **Clean Folder**: Cleans workspace, retrieves the source code from the specified Git repository, and checks out the specified branch.

2. **Hello**: Prints Docker container information.

3. **SonarQube Analysis**: Runs SonarQube scanner to perform static code analysis.

4. **Quality Gate**: Waits for the Quality Gate status from SonarQube, ensuring the code meets quality standards before proceeding.

5. **Docker**: Builds Docker image from the Dockerfile in the repository, tags it with the specified tag, pushes the image to Docker registry, and cleans up Docker images.

6. **File System Scan (FS SCAN)**: Scans the filesystem and Docker image for vulnerabilities using Aqua Security's Trivy.

7. **File System Scan (FS SCAN) Send**: Sends an email with the vulnerability scan results attached.

## Usage
1. Create a new pipeline job in Jenkins.
2. Copy the contents of the `Jenkinsfile` in this repository into the pipeline script section of the Jenkins job.
3. Configure the Jenkins job with the necessary credentials for accessing Git, Docker registry, and SonarQube.
4. Set up SonarQube webhook to trigger Quality Gate checks automatically.
5. Run the pipeline job to trigger the CI/CD process.

## Notes
- Replace placeholders such as `YOUR_GIT_URL`, `YOUR_SONARQUBE_INSTALLATION_NAME`, and `YOUR_DOCKER_REGISTRY_CREDENTIALS_ID` with actual values in the Jenkinsfile.
- Make sure to configure appropriate permissions and access controls for Jenkins, Docker, and SonarQube to ensure security and proper functioning of the pipeline.

## Support
If you encounter any issues or have questions regarding this Jenkins pipeline script, please feel free to open an issue in this repository or reach out via email at [arkyyy21@gmail.com](mailto:arkyyy21@gmail.com).

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
