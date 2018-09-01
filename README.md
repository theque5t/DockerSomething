
# DockerSomething

## Introduction

Anything and everything [Docker](https://www.docker.com/)

## Containers

[Rundeck](/rundeck)
- [ubuntu-16-04-rundeck-2-7-2-1](/rundeck/ubuntu-16-04-rundeck-2-7-2-1)
    * Description: [Rundeck](https://www.rundeck.com/what-is-rundeck) running on [Ubuntu](https://www.ubuntu.com). 
    * Instructions: Browse to the Rundeck url (default is http://localhost:4440) after container is started. Default credentials are admin/admin
    * OS: [Ubuntu 16.04](http://releases.ubuntu.com/16.04/)
    * Rundeck Version: [Rundeck 2.7.2-1](https://rundeck.org/docs/history/version-2.7.2.html)
    * Arguments:
        - PORT: Use `-e PORT=<port>` to change the listening port(default is 4440) for Rundeck
        - HOST: Use `-e HOST=<host>` to change the Rundeck URL(default is localhost)
    * Examples:
        - [Compose Build](https://docs.docker.com/compose/reference/build/)
        ```sh 
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-7-2-1> docker-compose build rundeck
        ```
        - [Compose Up](https://docs.docker.com/compose/reference/up/)
        ```sh
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-7-2-1> docker-compose up -d
        ```
        - [Compose Down](https://docs.docker.com/compose/reference/down/)
        ```sh
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-7-2-1> docker-compose down
        ```
        - Running in Parallel
            1. Create containers using `PORT` and `HOST` arguments(use unique values in PORT and HOST)
            ```sh
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-7-2-1> docker-compose run -d -p 4450:4450 -e PORT=4450 -e HOST=rundeck-2-7-2-1 rundeck
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-7-2-1> cd ..\ubuntu-16-04-rundeck-2-11-5-1\
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> docker-compose run -d -p 4451:4451 -e PORT=4451 -e HOST=rundeck-2-11-5-1 rundeck
            ```
            2. Add the HOST values to your hosts(e.g. `/etc/hosts` or `c:\Windows\System32\drivers\etc\hosts`) file, resolving to 127.0.0.1
            ```
            127.0.0.1 rundeck-2-7-2-1
            127.0.0.1 rundeck-2-11-5-1
            ```
            3. Both instances are now available via their unique URLs (`http://<host>:<port>`)
                * http://rundeck-2-7-2-1:4450
                * http://rundeck-2-11-5-1:4451
- [ubuntu-16-04-rundeck-2-11-5-1](/rundeck/ubuntu-16-04-rundeck-2-11-5-1)
    * Description: [Rundeck](https://www.rundeck.com/what-is-rundeck) running on [Ubuntu](https://www.ubuntu.com). 
    * Instructions: Browse to the Rundeck url (default is http://localhost:4440) after container is started. Default credentials are admin/admin
    * OS: [Ubuntu 16.04](http://releases.ubuntu.com/16.04/)
    * Rundeck Version: [Rundeck 2.11.5-1](https://rundeck.org/docs/history/version-2.11.5.html)
    * Arguments:
        - PORT: Use `-e PORT=<port>` to change the listening port(default is 4440) for Rundeck
        - HOST: Use `-e HOST=<host>` to change the Rundeck URL(default is localhost)
    * Examples:
        - [Compose Build](https://docs.docker.com/compose/reference/build/)
        ```sh 
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> docker-compose build rundeck
        ```
        - [Compose Up](https://docs.docker.com/compose/reference/up/)
        ```sh
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> docker-compose up -d
        ```
        - [Compose Down](https://docs.docker.com/compose/reference/down/)
        ```sh
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> docker-compose down
        ```
        - Running in Parallel
            1. Create containers using `PORT` and `HOST` arguments(use unique values in PORT and HOST)
            ```sh
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> docker-compose run -d -p 4450:4450 -e PORT=4450 -e HOST=something rundeck
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> docker-compose run -d -p 4451:4451 -e PORT=4451 -e HOST=somethingelse rundeck
            ```
            2. Add the HOST values to your hosts(e.g. `/etc/hosts` or `c:\Windows\System32\drivers\etc\hosts`) file, resolving to 127.0.0.1
            ```
            127.0.0.1 something
            127.0.0.1 somethingelse
            ```
            3. Both instances are now available via their unique URLs (`http://<host>:<port>`)
                * http://something:4450
                * http://somethingelse:4451

- [ubuntu-16-04-rundeck-3-0-1-20180803](/rundeck/ubuntu-16-04-rundeck-3-0-1-20180803)
    * Description: [Rundeck](https://www.rundeck.com/what-is-rundeck) running on [Ubuntu](https://www.ubuntu.com). 
    * Instructions: Browse to the Rundeck url (default is http://localhost:4440) after container is started. Default credentials are admin/admin
    * OS: [Ubuntu 16.04](http://releases.ubuntu.com/16.04/)
    * Rundeck Version: [Rundeck 3.0.1-20180803](https://rundeck.org/docs/history/version-3.0.1.html)
    * Arguments:
        - PORT: Use `-e PORT=<port>` to change the listening port(default is 4440) for Rundeck
        - HOST: Use `-e HOST=<host>` to change the Rundeck URL(default is localhost)
    * Examples:
        - [Compose Build](https://docs.docker.com/compose/reference/build/)
        ```sh 
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-3-0-1-20180803> docker-compose build rundeck
        ```
        - [Compose Up](https://docs.docker.com/compose/reference/up/)
        ```sh
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-3-0-1-20180803> docker-compose up -d
        ```
        - [Compose Down](https://docs.docker.com/compose/reference/down/)
        ```sh
        \DockerSomething\rundeck\ubuntu-16-04-rundeck-3-0-1-20180803> docker-compose down
        ```
        - Running in Parallel
            1. Create containers using `PORT` and `HOST` arguments(use unique values in PORT and HOST)
            ```sh
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> docker-compose run -d -p 4450:4450 -e PORT=4450 -e HOST=rundeck-2-11-5-1 rundeck
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-2-11-5-1> cd ..\ubuntu-16-04-rundeck-3-0-1-20180803\
            \DockerSomething\rundeck\ubuntu-16-04-rundeck-3-0-1-20180803> docker-compose run -d -p 4451:4451 -e PORT=4451 -e HOST=rundeck-3-0-1 rundeck
            ```
            2. Add the HOST values to your hosts(e.g. `/etc/hosts` or `c:\Windows\System32\drivers\etc\hosts`) file, resolving to 127.0.0.1
            ```
            127.0.0.1 rundeck-2-11-5-1
            127.0.0.1 rundeck-3-0-1
            ```
            3. Both instances are now available via their unique URLs (`http://<host>:<port>`)
                * http://rundeck-2-11-5-1:4450
                * http://rundeck-3-0-1:4451