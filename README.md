# SDH ORG Harvester Docker

Deploying and executing the __ORG Harvester__ of the *Smart Developer Hub* project with Docker.

## Usage instructions

### Building the Docker image

The first step consists in building the image defined by `Dockerfile` in the repository's root directory:

```bash
docker build -t sdh/org-harvester .
```

### Running the container


The *ORG Harvester* uses port 80, so when running the container it is important to expose it via the appropriate host port. For example, assuming that we want to make available the harvester via port 8088, we would execute the container as follows:

```bash
docker run -p 8088:80 \
           --name sdh-org-harvester \
           sdh/org-harvester
```

### License

SDH-ORG-Harvester-Docker is distributed under the Apache License, version 2.0.
