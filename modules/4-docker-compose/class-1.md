# Docker compose
![](../../media/module-4/docker_compose.png)
- ### Why you should use docker compose?
  - configure relationships between containers
  - save our docker container run settings in easy-to-read file
  - create one-liner developer environment startups
- ### What is docker compose?
  1. YAML-formatted file that describes our options for:
     1. containers
     2. networks
     3. volumes
  2. A CLI tool `docker compose` used for automatic the YAML from the point above

<hr>

### Useful commands and bits of commands:
`docker compose up`\
`docker compose up -d`\
`docker compose down`\
`docker compose ls`

## A. Now let's experiment with docker compose

### 1. Let's run the docker-compose example found in [compose-example](compose-example/docker-compose.yml)
### 2. Let's run the docker-compose example found in [compose-example-build](compose-example-build/docker-compose.yml)

## B. Now, let's replicate in docker compose some things we previously did in cli
### 1. Tuesday's [1st homework](../1-using-containers/homework.md)
### 2. [Today's Ventress exercise](../3-persistent-data/homework.md)

<hr>

#### Come back for the quiz after you finish with everything

<hr>

🌌 [DYOR: Advanced docker compose with secrets](https://blog.ruanbekker.com/blog/2017/11/23/use-docker-secrets-with-mysql-on-docker-swarm/)

<hr>

🌌 [And our next encounter is...](../5-container-registries/class-1.md)