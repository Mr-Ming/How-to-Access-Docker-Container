# How-to-Access-Docker-Container
How to access docker container


# Instruction
1) cd into the root of your docker.

2) Run `source .env && eval $(docker-machine env $DOCKER_MACHINE_NAME)`

3) List the docker container via `docker container ls`

<img width="414" alt="screen shot 2019-01-14 at 10 47 22 am" src="https://user-images.githubusercontent.com/2894340/51123342-e1863a80-17e9-11e9-8b5e-ca93e0262431.png">

4) Note the `CONTAINER ID` in the 1st column, this is what you use to access a docker container. Also, note the 2nd column `IMAGE`, this is the application that is running on that `CONTAINER ID`

5) To login to a `Redis` and open it into a new terminal you can do, `docker exec -i <CONTAINER ID> /bin/bash`.
Ex: `docker exec -it 002980906ab5 /bin/bash`

6) Afterward, then do `redis-cli` which open up `Redis`

7) Or you can do it the shortcut way. Instead of step 3 just do, `docker exec -i <CONTAINER ID> <BASH COMMAND>`.
Ex: `docker exec -it 002980906ab5 redis-cli`
