
1. How to search a docker image in hub.docker.com
```sh
docker search httpd
```
2. Download a docker image from hub.docker.com
```sh
docker image pull <image_name>:<image_version/tag>
```

3. List out docker images from your local system
```sh
docker image ls
```

4. Create/run/start a docker container from image
```sh
docker run -d --name <container_Name> <image_name>:<image_version/tag>

d - run your container in back ground (detached)
```

5. Expose your application to host server
```sh
docker run -d  -p <host_port>:<container_port> --name <container_Name> <image_name>:<Image_version/tag>

docker run -d --name httpd_server -p 8080:80 httpd:2.2
```

6. List out running containers
```sh
docker ps
```

7. List out all docker container (running, stpooed, terminated, etc...)
```sh
docker ps -a
```

8. Run a OS based container which interactive mode (nothing but login to container after it is up and running)

```sh
docker run -i -t --name centos_server centos:latest
i - interactive
t - Terminal
```

9. Stop a container 
```sh
docker stop <container_id>
```

10. Start a container which is in stopped or exit state

```sh
docker start <container_id>
```
11. Remove a container

```sh
docker rm <container_id>
```

12. Login to a docker container
```sh
docker exec -it <container_Name> /bin/bash
```

## What is Dockerfile

> A Dockerfile is set of instructions which are used to construct a Docker Image.

> These instructions are called directives.

## Dockerfile directives

> **FROM**: start a new build stage and sets the base image. usually must be the first directive in the Dockerfile (except ARG can be placed before FROM).

> **ENV**: set environment variables. These can be refefenced in the Dockerfile itself and are visible to the container at runtime. 

> **RUN**: creates a new layer on top of the previous layer by running a command inside that new layer and commiting the changes.

> **CMD**: specify a default command used to run a container at execution time.

> **EXPOSE**: documents which port(s) are intended to published when running a container

> **WORKDIR**: sets the current working directory for subsequent directives such as ADD, COPY, CMD, ENTRYPOINT, etc. Cna be used multiple time to change the directories throught the Dockerfile. you can also use relative path, which sets the new working direcotry relative to the previous working direcotry.
 
> **COPY**: copy files from the local machine to the image. 

> **ADD**: similar to COPY, but can also pull files using a URL and extract an archive into loose files in the image. 

> **STOPSIGNAL**: specify the signal that will be used to stop the container. 

> **HEALTHCHECK**: speciry a command to run in order to perform a custom health check to verify that the container is working properly.
