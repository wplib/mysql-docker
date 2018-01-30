# MySQL Docker Container for WPLib Box
This is the repository for the [mysql-docker](https://www.mysql.com/) Docker container implemented for [WPLib-Box](https://github.com/wplib/wplib-box).
It currently provides versions 5.5.59 5.6.39 5.7.21 8.0.3


## Supported tags and respective Dockerfiles

`8.0.3`, `8.0` _([8.0.3/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/8.0.3/Dockerfile))_

`5.7.21`, `5.7`, `latest` _([5.7.21/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/5.7.21/Dockerfile))_

`5.6.39`, `5.6` _([5.6.39/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/5.6.39/Dockerfile))_

`5.5.59`, `5.5` _([5.5.59/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/5.5.59/Dockerfile))_


## Using this container.
If you want to use this container as part of WPLib, then use the Docker Hub method.
Or you can use the GitHub method to build and run the container.


## Using it from Docker Hub

### Setup from Docker Hub
A simple `docker pull wplib/mysql` will pull down the latest version.


### Runtime from Docker Hub
start - Spin up a Docker container with the correct runtime configs.

`docker run -d --name wplib_mysql_8.0.3 --restart unless-stopped --network wplibbox -p 3306:3306 -v /tmp/sql:/docker-entrypoint-initdb.d -v mysql_data:/var/lib/mysql wplib/mysql:8.0.3`

stop - Stop a Docker container.

`docker stop wplib_mysql_8.0.3`

run - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.

`docker run --rm --name wplib_mysql_8.0.3 --network wplibbox -p 3306:3306 -v /tmp/sql:/docker-entrypoint-initdb.d -v mysql_data:/var/lib/mysql wplib/mysql:8.0.3`

shell - Run a shell, (/bin/bash), within a Docker container.

`docker run --rm --name wplib_mysql_8.0.3 -i -t --network wplibbox -p 3306:3306 -v /tmp/sql:/docker-entrypoint-initdb.d -v mysql_data:/var/lib/mysql wplib/mysql:8.0.3 /bin/bash`

rm - Remove the Docker container.

`docker container rm wplib_mysql_8.0.3`


## Using it from GitHub repo

### Setup from GitHub repo
Simply clone this repository to your local machine

`git clone https://github.com/wplib/mysql-docker.git`


### Building from GitHub repo
`make build` - Build Docker images. Build all versions from the base directory or specific versions from each directory.


`make list` - List already built Docker images. List all versions from the base directory or specific versions from each directory.


`make clean` - Remove already built Docker images. Remove all versions from the base directory or specific versions from each directory.


`make push` - Push already built Docker images to Docker Hub, (only for WPLib admins). Push all versions from the base directory or specific versions from each directory.


### Runtime from GitHub repo
When you `cd` into a version directory you can also perform a few more actions.

`make start` - Spin up a Docker container with the correct runtime configs.


`make stop` - Stop a Docker container.


`make run` - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.


`make shell` - Run a shell, (/bin/bash), within a Docker container.


`make rm` - Remove the Docker container.


