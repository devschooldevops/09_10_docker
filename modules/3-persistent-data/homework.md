
**Task name:** Database upgrade with containers

Task instructions:
- create a `postgres` container with a named volume `r2d2-data` using version `13.7`
- use Docker Hub to see what the `VOLUME` path is in the Dockerfile and how to run it
- check the logs to see if the database starts correctly, then stop the container
- create a new `postgres` container using version `13.8` with the same `r2d2-data` volume
- check logs to validate everything started up correctly

<hr>

🌌 **[Next stop: docker compose](../4-docker-compose/class-1.md)**