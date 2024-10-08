# docker-compose-test
Dev container based initial set up for python enviroment.
--------
Intial setup with Dockerfile.

--------
2nd by using docker-compose.yml

1) create .devcontiner folder and devcontainer.json to define path for docker-compose.yaml
2) docker-compose.yml file contains the services for example - app and db
VSCODE - Ctrl+shft+p
Dev continer: rebuild and reopen continer.
--------
3nd docker-compose and Dockerfile.

1)Instead of using image path of python setup/env. in docker-compose.yml, create a Dockerfile and set path in Dockerfile.

example-
Dockerfile
FROM python:3
RUN mkdir /workspace
WORKDIR /workspace
CMD [ "python"]

docker-compose.yml
services:
  app:
    #image:mcr.microsoft.com/devcontainers/python:dev-3.12-bookworm
    build:
      context:.