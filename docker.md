# Docker Notes

## Logs

To read the logs of a container  
`docker logs <container_name>`

You can read the logs live  
`docker logs -f <container_name>`

## Interact with the container

You can execute commands inside the container  
`docker exec -it <container_name> <command>`

To open an interactive shell with the container  
`docker exec it <container> /bin/bash`

## Build Containers

To build a container follow the steps below

1-  Create a file `Dockerfile`

2-  Inside that file write the docker instructions  
```
FROM <image>
CMD ["echo","Hello there, i am a running image"]
```
3- Run `docker build .` . This means that build from the instruction file that is here. Docker will search for the `Dockefile` and execute what is inside it.

4- Check the container ID from `docker ps`

5- Run the container `docker run <container_ID>`

## Help

To know the available commands  
`docker --help`

To know get the help for a specific command  
`docker <command> --help`