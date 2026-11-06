# 1. Install Jenkins on DigitalOcean

## Steps completed

- Created a DigitalOcean server to host Jenkins.
- Set up Docker on the server so Jenkins can run in a container.
- Started Jenkins as a Docker container and exposed its web interface.
- Completed the initial Jenkins setup and prepared it for creating build jobs.

<br>

# 2. Create a CIPipeline with Jenkinsfile (Freestyle, Pipeline, Multibranch Pipeline)

## Technologies used

- Jenkins
- Docker
- DigitalOcean
- Linux
- Git
- Java
- Maven

<br>

## Build Jar File

<br>

![Successful Maven build](images/build-success.png)
_Successful Maven test and package build._

<br>

![Jenkins job output](images/commands-executed.png)
_Jenkins job running the configured build commands._

<br>

## Build image

![Build-image stage](images/build-image.png)
_Build-image stage added to the CI flow._

![Docker image build output](images/image-built.png)
_Docker image built successfully._

![Docker image verification](images/image-verification.png)
_Created Docker image verified locally._

<br>

## Push to private Docker repository

![Push-to-repository stage](images/push-to-repository.png)
_Push-to-repository stage added to the CI flow._

![Successful Docker push](images/success-push.png)
_Docker image pushed successfully to the private repository._

![Docker Hub repository](images/image-in-dockerhub.png)
_Published image available in Docker Hub._

<br>

## Push to Nexus repository

![Successful Nexus push](images/push-to-nexus.png)
_Docker image pushed successfully to the Nexus repository._

![Nexus repository image](images/nexus-image.png)
_Published Java Maven image available in Nexus._

<br>
