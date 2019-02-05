# docker-app: nextcloud

[![Docker Automated build](https://img.shields.io/docker/automated/talsenteam/docker-nextcloud.svg?style=for-the-badge)](https://hub.docker.com/r/talsenteam/docker-nextcloud/)
[![Docker Pulls](https://img.shields.io/docker/pulls/talsenteam/docker-nextcloud.svg?style=for-the-badge)](https://hub.docker.com/r/talsenteam/docker-nextcloud/)
[![Docker Build Status](https://img.shields.io/docker/build/talsenteam/docker-nextcloud.svg?style=for-the-badge)](https://hub.docker.com/r/talsenteam/docker-nextcloud/)

The server application nextcloud ready to run inside a docker container.

[![Docker Automated build](https://img.shields.io/docker/automated/talsenteam/docker-nextcloud-database.svg?style=for-the-badge)](https://hub.docker.com/r/talsenteam/docker-nextcloud-database/)
[![Docker Pulls](https://img.shields.io/docker/pulls/talsenteam/docker-nextcloud-database.svg?style=for-the-badge)](https://hub.docker.com/r/talsenteam/docker-nextcloud-database/)
[![Docker Build Status](https://img.shields.io/docker/build/talsenteam/docker-nextcloud-database.svg?style=for-the-badge)](https://hub.docker.com/r/talsenteam/docker-nextcloud-database/)

An utility application for nextcloud ready to run inside a docker container.

## how to use

work-in-progress

## custom VS Code tasks

Any docker-compose--* tasks refer to the default dockerfile [nextcloud](docker/server--nextcloud/default.docker) and [nextcloud-database](docker/server--nextcloud-database/default.docker) as well as to the [docker-compose](docker-compose/server--nextcloud/default.docker-compose) configuration if required for command execution.

- browser--*
  - [browser--open-application-url](bash-commands/browser--open-application-url.sh)  
    Opens the localhost docekr service URL in the default web-browser. The opened URL is defined in [host.env](host.env) by the variable HOST_SERVICE_URL.
- docker-compose--*
  - docker-compose--compose--*
    - [docker-compose--compose--create](bash-commands/docker-compose--compose--create.sh)  
      Creates required docker containers and docker networks but does not start them.
    - [docker-compose--compose--down](bash-commands/docker-compose--compose--down.sh)  
      Stops and removes required docker containers and docker networks.
    - [docker-compose--compose--up](bash-commands/docker-compose--compose--up.sh)  
      Creates and starts required docker containers and docker networks.
  - docker-compose--container--*
    - [docker-compose--container--kill](bash-commands/docker-compose--container--kill.sh)  
      Kills all running containers declared by the compose configuration.
    - [docker-compose--container--restart](bash-commands/docker-compose--container--restart.sh)  
      Restarts all containers declared by the compose configuration (if they were created before).
    - [docker-compose--container--start](bash-commands/docker-compose--container--start.sh)  
      Starts all containers declared by the compose configuration (if they were created before).
    - [docker-compose--container--stop](bash-commands/docker-compose--container--stop.sh)  
      Stops all running containers declared by the compose configuration.
  - docker-compose--image--*
    - [docker-compose--image--build](bash-commands/docker-compose--image--build.sh)  
      Builds all required docker images referenced by the compose configuration (using build cache).
    - [docker-compose--image--rebuild](bash-commands/docker-compose--image--rebuild.sh)  
      Builds all required docker images referenced by the compose configuration (without using build cache).
  - docker-compose--log--*
    - [docker-compose--log--container-info](bash-commands/docker-compose--log--container-info.sh)  
      Prints general conntainer informations regarding the compose configuration to the console.
    - [docker-compose--log--container-log](bash-commands/docker-compose--log--container-log.sh)  
      Prints logs of running containers declared by the compose configuration to the console.
  - docker-compose--system--*
    - [docker-compose--system--clean](bash-commands/docker-compose--system--clean.sh)  
      Removes local dangling docker containers, images and networks.
    - [docker-compose--system--prune](bash-commands/docker-compose--system--prune.sh)  
      Prunes the local docker system.
  - docker-compose--volumes--*
    - [docker-compose--volumes--wipe-local](bash-commands/docker-compose--volumes--wipe-local.sh)  
      Wipes local volume mapping directories, located in the subdirectory 'volumes/', if there are any.
- git--*
  - [git--pull-and-update-submodules](bash-commands/git--pull-and-update-submodules.sh)  
    Rebase pulls the latest repository changes and the updates all git submodules if there are any.
