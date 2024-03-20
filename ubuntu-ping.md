# Ubuntu mit ping 

```
cd
mkdir myubuntu 
cd myubuntu/
```

```
# nano Dockerfile
FROM ubuntu:latest
RUN apt-get update; apt-get install -y inetutils-ping
CMD ["/bin/bash"]
```

```
docker build -t myubuntu .
docker images
```

```
# -t wird benötigt, damit bash WEITER im Hintergrund im läuft.
# auch mit -d (ohne -t) wird die bash ausgeführt, aber "das Terminal" dann direkt beendet 
# -> container läuft dann nicht mehr 
docker run -d -t --name container-ubuntu myubuntu
docker container ls
```

```
## Optional 
# in den container reingehen mit dem namen des Containers: myubuntu 
docker exec -it myubuntu bash
ls -la
exit
```

```
# Zweiten Container starten
docker run -d -t --name container-ubuntu2 myubuntu
# ip rausfinden von 2. container 
docker network inspect bridge 
```

```
# In 2. Container mit exec reingehen -> Ersten Container -> 2. anpingen 
docker exec -it container-ubuntu bash 
# Jeder container hat eine eigene IP 
ping 172.17.0.3
```
