# Persistent Data
## We will learn about:
- Top problems of persistent data
- Container concepts: immutable, ephemeral
- How to use Docker Hub image registry
- Data Volumes
- Bind Mounts

<hr>

### [Top problems of persistent data](https://www.pegasusone.com/persistant-data-storage-docker-kubernetes/)
- App - storage coupling
- Data integrity
- Data agility considering upgrades
### Data Volumes
#### Let's go to [https://hub.docker.com](https://hub.docker.com), download a database image (mysql, mariadb, cassandra, etc) and run some containers
We will create, delete, view and mount named and unnamed volumes

### Bind Volumes
#### Let's go to [06_docker/modules/2-container-images/dockerfile-example-2](../2-container-images/dockerfile-example-2)
And let's run the same container with a bind volume and do some editing and adding files trickery

### Useful commands and bits of commands:
`docker volume create <name>`\
`docker volume list <name>`\
`docker volume prune <name>`\
`docker volume inspect <name>`

<hr>

### Go back to the quiz

<hr>

🌌 **[Ventress is advancing with her troops! Go fight her before we lose our headquarters!](homework.md)**
