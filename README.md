### Hexlet tests and linter status:
[![Actions Status](https://github.com/amarynets/devops-for-programmers-project-74/workflows/hexlet-check/badge.svg)](https://github.com/amarynets/devops-for-programmers-project-74/actions)
[![Actions Status](https://github.com/amarynets/devops-for-programmers-project-74/workflows/push/badge.svg)](https://github.com/amarynets/devops-for-programmers-project-74/actions/workflows/push.yml)

Required OS: MacOS, Linux, Windows + WSL2

This repository contains fastify application with docker compose files to start this application in production & test mode.

Exectuion:
There are follow environment variables that are used by the docker compose to run the application:
```
DATABASE_NAME - the name of the database (by default "postgres")
DATABASE_USERNAME - username of the database (by default "postgres")
DATABASE_PASSWORD - by default the password is "password"
DATABASE_PORT - port for the db container (default if 5432)
```

To start the production mode just run docker compose up in the root directory. This will start up the Postresql DB, Caddy reverse proxy and the application itself. You can also use Makefile command make start.

To start tests for this application, you can run: make ci.

The docker image for this application is hosted on docker hub - [amarynets/devops-for-programmers-project-74](https://hub.docker.com/r/amarynets/devops-for-programmers-project-74) (docker pull amarynets/devops-for-programmers-project-74)