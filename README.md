# roboshop-docker

Networking:
If we want to check ip information: ifconfig 

When docker is installed a default interface called docker0 is created which gives the IP address to the containers.

docker network ls
 bridge --docker by default uses bridge network
 host -- 

 docker run --network host nginx

Default bridge network containers can't communicate with each other

docker network
docker network create roboshop
docker network ls

docker network disconnect bridge mongodb

docker network disconnect bridge catalogue

docker network connect roboshop mongodb
docker network connect roboshop catalogue

ifconfig

docker inspect mongodb

docker exec -it catalogue bash
curl http://localhost:80/health



