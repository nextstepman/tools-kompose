Kubernetes Kompose in a (docker) box. 

# Supported tags and respective `Dockerfile` links

-	[`latest`](https://github.com/nextstepman/tools-kompose/blob/master/Dockerfile): contains ubuntu:xenial with current (1.16.0) kompose installed to it

# Usage

## Quick start

The intended use is to start this image, mount a volume and run kompose from there. 
You can mount your current workdir to the /home/kompose/workdir folder (or other folder as you like) to allow kompose to access your local docker-compose files.

```
docker run -it --rm -v `pwd`:/home/kompose/workdir nextstepman/tools-kompose:latest
```

Or make that an alias like this in your profile:

```
alias kompose="docker run -it --rm -v \$(pwd):/home/kompose/workdir nextstepman/tools-kompose:latest"
```

