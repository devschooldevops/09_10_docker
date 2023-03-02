# Using containers
## We will learn about:
- What is a container?
- How to run a container?
- How to start/stop/remove/inspect a container?
- Shell inside container
- [Networking](class-2.md)
<hr>

### What happens when we run `docker container run`
1. Looks for that image locally in image cache, doesn't find anything
2. Then looks in remote image repository (default Docker Hub)
3. Downloads the latest version (nginx:latest by default)
4. Creates new contianer based on that image and prepares to start
5. Gives it a virtual IP on a private network inside docker engine
6. Opens up port 80 on host and forwards to port 80 in container
7. Starts container by using the CMD in the image Dockerfile

#### Useful commands and bits of commands:
`docker container run -p 80:80 nginx`\
`docker image pull <name>`\
`--publish, -p`\
`--detach, -d`\
`docker container ps -a`\
`--name`\
`docker container logs -f <name>`\
`docker container stop <name>`\
`docker container start <name>`\
`docker container rm <name>`\
`docker container run -it --name nginx nginx bash`\
Above command starts a new container interactively\
`docker container exec -it nginx bash`\
Above command runs additional command in existing container

<hr>

### Go to the [quiz](https://kahoot.it/)

<hr>

🌌 **[Let's continue](class-2.md)**