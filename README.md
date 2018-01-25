# MySQL Docker Container for wplib
This is the repository for the [mysql-docker](https://www.mysql.com/) Docker container implemented for [WPLib-Box](https://github.com/wplib/wplib-box).
It currently provides versions 5.5.59 5.6.21 5.7.21 8.0.3


## Supported tags and respective Dockerfiles

`8.0.3` , `8.0.3` _([8.0.3/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/8.0.3/Dockerfile))_

`5.7.21` , `5.7.21`, `latest` _([5.7.21/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/5.7.21/Dockerfile))_

`5.6.39` , `5.6.39` _([5.6.39/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/5.6.39/Dockerfile))_

`5.5.59` , `5.5.59` _([5.5.59/Dockerfile](https://github.com/wplib/mysql-docker/blob/master/5.5.59/Dockerfile))_


## Setup
Simply clone this repository to your local machine

`git clone https://github.com/wplib/mysql-docker.git`

and run either...


### Building all images
`make build`


### Listing all built images
`make list`


### Cleaning all images
`make clean`
