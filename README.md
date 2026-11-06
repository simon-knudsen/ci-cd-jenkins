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
*Build-image stage added to the CI flow.*

![Docker image build output](images/image-built.png)
*Docker image built successfully.*

![Docker image verification](images/image-verification.png)
*Created Docker image verified locally.*

## Push to private docker repository
