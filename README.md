# Minimal Docker image with Oracle Server JRE 8 w/ Unlimited Java Cryptography Extension

This image is based on Alpine Linux 3.4 to keep the size low and provides additional security.
All Alpine provided userland binaries are compiled as Position Independent Executables (PIE)
with stack smashing protection. Image includes BASH and cURL.

* Oracle Server JRE Version: 8u112b15

Download automated build from public Docker Hub Registry: docker pull platten/alpine-oracle-jre8-docker

## Usage Example:
` docker run -it --rm platten/alpine-oracle-jre8-docker java -version `

## Example Dockerfiles for your own project:

```
FROM platten/alpine-oracle-jre8-docker

WORKDIR /src
RUN curl -o hello.jar https://raw.githubusercontent.com/apcera/sample-apps/master/example-java-jar-hello/hello.jar

CMD java -jar hello.jar
```
