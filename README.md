# docker

Common docker commands used for working and interacting with images.

### To pull specific version of image

`docker pull <image_name>:<tag>`

`docker pull confluentinc/cp-enterprise-kafka:5.5.1`

### List the images 

`docker images`

### Remove any image
`docker rmi `

### Remove any container
`docker rm`

### Stop any container
`docker stop`


### Command to start any container with specific network and parameters.
`docker run -d --name zookeeper-server --network kafka-net -e ALLOW_ANONYMOUS_LOGIN=yes bitnami/zookeeper:latest`

`docker run -d --name kafka-server --network kafka-net -e ALLOW_PLAINTEXT_LISTENER=yes -e KAFKA_CFG_ZOOKEEPER_CONNECT=zookeeper-server:2181 bitnami/kafka:2.4.1`

`docker run --name zookeeper --network kafka-net  -e ALLOW_ANONYMOUS_LOGIN=yes -p 2181:2181 bitnami/zookeeper:latest`

### Start the containers with docker-compose, go to directory having docker-compose.yml file and run below command
`docker-compose up -d --build`

### To stop and remove containers:
`docker-compose down `

### Connect to container in interactive way using bash
`docker exec -it --user root <CONTAINER ID> bash`


