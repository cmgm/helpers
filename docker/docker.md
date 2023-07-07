

# Commands 

## Run 
docker run   -d  --rm --name jupyter_lab \
-p 8889:8888  \
-e JUPYTER_TOKEN=cmgm   \
-v /$HOME/apps/jupypter_exp:/app  \
jupyter_lab



### Processes
docker ps

### interactive session in container 


### 

## Images 
docker image ls -a


## Containers

## Networks 

## Volumes 


# links  ------------------------------------------------------

## docker compose file spec
https://github.com/compose-spec/compose-spec/blob/master/spec.md



# clean images and containers  fast 

docker image ls  -a

docker image ls -a  | awk 'NR > 1 {print " "$3" "}' | xargs -n 1 docker image rm -f 

docker container ls -a
docker container ls -a  | awk 'NR > 1 {print " "$1" "}' | xargs -n 1 docker container rm -f 

docker volume  ls 

274762424897-compute@developer.gserviceaccount.com


# interactive sesseion

docker exec -it  elegant_nash  /bin/bash

