

# run  

docker run -d --hostname my-rabbit --name some-rabbit rabbitmq:3

docker logs some-rabbit


docker run -d --hostname my-rabbit --name some-rabbit -e RABBITMQ_DEFAULT_USER=user -e RABBITMQ_DEFAULT_PASS=password rabbitmq:3-management

docker run -d --hostname my-rabbit --name some-rabbit -p 8080:15672 rabbitmq:3-management


# links 
https://hub.docker.com/_/rabbitmq


