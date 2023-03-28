# Persistent Data
## We will learn about:
- Top problems of persistent data
- Container concepts: immutable, ephemeral
- Data Volumes
- Bind Mounts

<hr>

### [Top problems of persistent data](https://www.pegasusone.com/persistant-data-storage-docker-kubernetes/)
- App - storage coupling
- Data integrity
- Data agility considering upgrades

### Useful commands and bits of commands:
`docker volume create <name>`\
`docker volume list <name>`\
`docker volume prune <name>`\
`docker volume inspect <name>`

### Step 1: Let's go inside the [getting-started/app](getting-started/app) directory and build our docker image:
`docker build -t todo .`

Let's run and play with it a bit:\
`docker run --name todo -dp 3000:3000 todo`\
`docker container rm -f todo`

### Data Volumes
Let's create a volume and attach it to our container\
Our database file is located in `/etc/todos`. We will attach our volume to that location internally\
`docker volume create todo-db`\
`docker run --name todo -dp 3000:3000 -v todo-db:/etc/todos todo`

### Let's create 2 other containers. One *with the same volume*, and another one *without a volume*

`docker run --name ex1 -dp 3001:3000 -v todo-db:/etc/todos todo`\
`docker run --name ex2 -dp 3002:3000 todo`

Let's see the difference between those
`docker container inspect ex1 ex2 | grep -i -A 5 mounts`

### Bind Volumes
First, `cd` into `getting-started/app` if didn't already

Then, run:\
`docker run -it -v ${PWD}:/src alpine sh`\
This will download a lightweight linux distro and mount the *host* `PWD` directory inside the `/src` *container* directory

See how you can modify, add and delete files from your system.
Is the reversible true? Can you also modify them from inside the container?
Yes you can, try.

<hr>

### Go to the [quiz](https://kahoot.it/)

<hr>

🌌 **[Ventress is advancing with her troops! Go fight her before we lose our headquarters!](homework.md)**
