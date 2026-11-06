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

## Freestyle pipeline

<br>

### Build Jar File

<br>

![Successful Maven build](images/build-success.png)
_Successful Maven test and package build._

<br>

![Jenkins job output](images/commands-executed.png)
_Jenkins job running the configured build commands._

<br>

### Build image

![Build-image stage](images/build-image.png)
_Build-image stage added to the CI flow._

<br>

![Docker image build output](images/image-built.png)
_Docker image built successfully._

<br>

![Docker image verification](images/image-verification.png)
_Created Docker image verified locally._

<br>

### Push to private Docker repository

![Push-to-repository stage](images/push-to-repository.png)
_Push-to-repository stage added to the CI flow._

<br>

![Successful Docker push](images/success-push.png)
_Docker image pushed successfully to the private repository._

<br>

![Docker Hub repository](images/image-in-dockerhub.png)
_Published image available in Docker Hub._

<br>

### Push to Nexus repository

![Successful Nexus push](images/push-to-nexus.png)
_Docker image pushed successfully to the Nexus repository._

<br>

![Nexus repository image](images/nexus-image.png)
_Published Java Maven image available in Nexus._

<br>

## Pipeline

The freestyle build steps were replaced with a declarative Jenkins pipeline, which keeps the CI flow defined as code. The pipeline checks out the source code, installs the required tools, and then runs the build app, build image, and deploy stages.

![Completed Jenkins pipeline](images/pipeline-completed-1.png)
_Jenkins Stage View showing a successful `my-pipeline` run, with all stages completed._
