# Creating a `Dockerfile`

A `Dockerfile` is a text file that contains a set of instructions for building a Docker image. It is used to automate the process of creating a Docker image by specifying the base image, adding files, installing packages, and configuring the environment

The `Dockerfile` instruction syntax is defined by the specification reference in the `Dockerfile` reference:

<https://docs.docker.com/engine/reference/builder/>

Here are the most common types of instructions:

- **FROM**: Defines a base for your image.
- **RUN**: Executes any commands in a new layer on top of the current image and commits the result. RUN also has a shell form for running commands.
- **WORKDIR**: Sets the working directory for any RUN, CMD, ENTRYPOINT, COPY, and ADD instructions that follow it in the Dockerfile.
- **COPY**: Copies new files or directories from `<src>` and adds them to the filesystem of the container at the path `<dest>`.
- `CMD`: Lets you define the default program that is run once you start the container based on this image.

In addition to the `Dockerfile`, there are other files used in the Docker ecosystem, such as the `docker-compose.yml file`, which is used to define and run multi-container Docker applications

The name of the `Dockerfile` is commonly `Dockerfile` but it can be named whatever you like.

To write an efficient `Dockerfile`, it is important to follow some best practices, such as using a minimal base image, consolidating RUN statements, using multi-stage builds, and using explicit and deterministic Docker base image tags

`Dockerfile` can be used to package software and automate the deployment of software in lightweight containers. Docker builds images automatically by reading the instructions from a `Dockerfile`, which is a text document that contains all the commands a user could call on the command line to assemble an image

To specify the base image in a `Dockerfile`, you can use the FROM instruction followed by the name of the base image. For example, to use the Ubuntu 22.04 base image, you can use the following instruction:

```Dockerfile
FROM ubuntu:22.04
```

When specifying dependencies in a Dockerfile, it is important to avoid some common mistakes, such as using the latest tag for the base image, installing unnecessary packages, and not cleaning up after package installation

Another common command you will use is:

`EXPOSE`: Specifies the port that the container listens on.

The EXPOSE instruction in a Dockerfile informs Docker that the container listens on the specified network ports at runtime.

It does not actually publish the specified ports to the host machine or make them accessible to the outside world. Instead, it is a way for the person who built the image to communicate to the person who will run the container, which port the service inside the container will listen to

To actually publish the ports and make them accessible to the outside world, you need to use the -p or --publish flag when running the container

For example, to publish port 80 on the container to port 8080 on the host machine, you can use the following command:

`docker run -p 8080:80 myimage`

When specifying dependencies in a Dockerfile, it is important to avoid some common mistakes, such as using the latest tag for the base image, installing unnecessary packages, and not cleaning up after package installations
