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

## Steps completed

- Created CI jobs in Jenkins using Freestyle, Pipeline, and Multibranch Pipeline job types.
- Installed and configured the build tools required by the project, including Maven.
- Made Docker available to Jenkins so the pipeline can build container images.
- Added Jenkins credentials for the Git repository and Docker Hub.
- Connected Jenkins jobs to this Java Maven application repository.
- Added a `Jenkinsfile` to define the pipeline as code.
- Built the Maven application into a JAR file during the pipeline.
- Built a Docker image containing the generated application JAR.
- Tagged and pushed the image to a private Docker Hub repository.

<br>

### Pipeline stages

- **Initialize:** Load the shared pipeline script used by the Jenkinsfile.
- **Build JAR:** Run Maven to package the Java application.
- **Build image:** Build the Docker image and authenticate with Docker Hub using Jenkins credentials.
- **Deploy:** Keep a deployment stage ready for the next delivery step.

<br>

![CI pipeline flow](images/CleanShot%202026-11-06%20at%2010.00.17.png)
_CI flow: checkout, test, and build the JAR._

<br>

![Successful Maven build](images/build-success.png)
_Successful Maven test and package build._

<br>

![Jenkins job output](images/commands-executed.png)
_Jenkins job running the configured build commands._

<br>
