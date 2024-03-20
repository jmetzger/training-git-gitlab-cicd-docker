# 2 Containers with Network and Ping

## Container 1:

```
docker run --name dockerserver1 -dit ubuntu
```

## Container 2:

```
docker run --name dockerserver2 -dit ubuntu
```

## Netzwerk anschauen 

```
docker network ls
docker network inspect bridge
# dockerserver1 - 172.17.0.2
# dockerserver2 - 172.17.0.3
```

## Auf einen der Server rauf 

```
docker container ls
docker exec -it dockerserver1 bash
# im container 
apt update; apt install -y iputils-ping 
ping 172.17.0.3 
```
