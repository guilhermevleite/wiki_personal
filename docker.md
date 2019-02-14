# Docker

## Architecture

**Docker Registry** keeps all the docker images, the hub. When commands such as 
docker pull or docker run are executed, the image is fetched from the hub.

**Docker Image** is read-only template with instructions to create a docker
container. An image can be based on another one, such as an image that is based
on the ubuntu image. When an image in built, only the changed layers are
rebuilt, keeping images lightweighted.

**Docker Container** is the runable instance of an image. They are created, moved,
started, or stoped. It is possible to create a new image based on the
container's current state.

### Example

> docker run -i -t ubuntu /bin/bash
Will actually runs docker pull ubuntu, docker container create, and start it.

## DockerFile

The linux command 'execute' will not last between the phases of docker building
process. Use ENV instead.

## Trouble Shooting

* Permission denied when accessing docker daemon:
> sudo usermod -a -G docker $USER
