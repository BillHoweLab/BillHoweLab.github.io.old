# Lab Website Setup and Contribution Instructions

## Local setup using Docker (Recommended)
Using Docker to install Jekyll and Ruby dependencies is the easiest way.

You need to take the following steps to get the website up and running on your local machine:

- Install [Docker Desktop](https://docs.docker.com/get-docker/). As of Sept 2023, Docker Compose is automatically installed with Docker Desktop, but if not on your machine, install [docker-compose](https://docs.docker.com/compose/install/).
- Run the following command that will pull the latest pre-built image from DockerHub and will run your website.

```bash
$ docker-compose up
```
Note that when you run it for the first time, it will download a docker image of size 400MB or so.

After you are done editing, you can use the same command (`docker-compose up`) to render the webpage with all you changes. Also, make sure to commit your final changes.

> To change port number, you can edit `docker-compose.yml` file.
