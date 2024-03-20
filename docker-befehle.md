# Übersicht docker befehle 

```
# docker hub durchsuchen
docker search hello-world

docker run <image>
# z.b. // Zieht das image aus docker hub 
# hub.docker.com 
docker run hello-world

# logs anzeigen
docker logs <container-id>
docker logs <container-name>

# images die lokal vorhanden 
docker images 

# configuration des containers
docker inspect <container-id>

# container (laufende) 
docker container ls 
# container (vorhanden, aber beendet)
docker container ls -a 

# z.b hilfe für docker run 
docker help run 

 


```
