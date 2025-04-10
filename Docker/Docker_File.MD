
## What is Dockerfile

> A Dockerfile is set of instructions which are used to construct a Docker Image.

> These instructions are called directives.

## Dockerfile directives

> **FROM**: Start a new build stage and sets the base image. usually must be the first directive in the Dockerfile (except ARG can be placed before FROM).

> **ENV**: Set environment variables. These can be referenced in the Dockerfile itself and are visible to the container at runtime. 

> **RUN**: Creates a new layer on top of the previous layer by running a command inside that new layer and committing the changes.

> **CMD**: Specify a default command used to run a container at execution time.

> **EXPOSE**: Documents which port(s) are intended to published when running a container

> **WORKDIR**: Sets the current working directory for subsequent directives such as ADD, COPY, CMD, ENTRYPOINT, etc. Can be used multiple time to change the directories throught the Dockerfile. You can also use relative path, which sets the new working direcotry relative to the previous working directory.
 
> **COPY**: Copy files from the local machine to the image. 

> **ADD**: Similar to COPY, but can also pull files using a URL and extract an archive into loose files in the image. 

> **STOPSIGNAL**: Specify the signal that will be used to stop the container. 

> **HEALTHCHECK**: Specify a command to run in order to perform a custom health check to verify that the container is working properly.
