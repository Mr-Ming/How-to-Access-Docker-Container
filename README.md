# How-to-Access-Docker-Container
How to access docker container


# Instruction
1) cd into the root of your docker.

2) Run `source .env && eval $(docker-machine env $DOCKER_MACHINE_NAME)`

3) List the docker container via `docker container ls`

![screen shot 2019-01-14 at 10 19 44 am](https://user-images.githubusercontent.com/2894340/51121661-f365de80-17e5-11e9-965a-40180875802e.png)

4) Note the `CONTAINER ID` in the 1st column, this is what you use to access a docker container. Also, note the 2nd column `IMAGE`, this is the application that is running on that `CONTAINER ID`

5) To login to a `Redis` and open it into a new terminal you can do, `docker exec -i <CONTAINER ID> /bin/bash`.
Ex: `docker exec -it 002980906ab5 /bin/bash`

6) Afterward, then do `redis-cli` which open up `Redis`

![screen shot 2019-01-14 at 10 25 48 am](https://user-images.githubusercontent.com/2894340/51121996-cf56cd00-17e6-11e9-85b6-addb67bfab65.png)

7) Or you can do it the shortcut way. Instead of step 3 just do, `docker exec -i <CONTAINER ID> <BASH COMMAND>`.
Ex: `docker exec -it 002980906ab5 redis-cli`

![screen shot 2019-01-14 at 10 28 00 am](https://user-images.githubusercontent.com/2894340/51122105-1b097680-17e7-11e9-992e-33855f4abc75.png)
