# markhobson/maven-firefox

Docker image for Java automated UI tests.

Includes:

* JDK 8/11/17/21
* Maven 3.9.10
* Firefox 147
* Geckodriver 0.36.0

Available on [Docker Hub](https://hub.docker.com/r/markhobson/maven-firefox/).

## Tags

The following Docker tags are available:

* `jdk-8` [(jdk-8/Dockerfile)](jdk-8/Dockerfile)
* `jdk-11` [(jdk-11/Dockerfile)](jdk-11/Dockerfile)
* `jdk-17`, `latest` [(jdk-17/Dockerfile)](jdk-17/Dockerfile)
* `jdk-21`, `latest` [(jdk-21/Dockerfile)](jdk-21/Dockerfile)

## Demo

See the [demo](demo) Maven project to see how this Docker image can be used to run UI tests. The [run.sh](demo/run.sh) script builds the project within the latest version of this image on Docker Hub.
