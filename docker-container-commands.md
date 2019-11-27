### list containers 
```sh
  docker container ls -a 
```

### start specified container
```sh
  docker container start <container>
```
  
### delete container 
```sh
docker container rm <container>
docker container rm 62eae76ed8a1 431da1eeb3b3 1c0f526b133b 68ffa05621ee 
```

### create container of nginx, detach it, name it and map host port 8080 to 80
```sh
  docker container run --publish 8080:80 --detach --name rajiv-nginx-1 nginx
```

### kill the specified container (only the first few characters of container id to identify it uniquely)
```sh
  docker container kill 66
```

### start a container (by default it will be detached)
```sh
  docker container start rajiv-nginx-1 
```

### start an existing container by attaching STDIO and interactively 
```sh
  docker container start -ai rajiv-nginx-2
```

### show the port mappings of this container
```sh
  docker container port rajiv-nginx-1 
```

### list processes running in the specified container
```sh
  docker container top rajiv-nginx-1 
 ```
  
### list docker images
```sh 
  docker images 
```

### show various stats of running container like cpu and memory usage on a real time basis like linux top command
```sh
docker container stats 
```

### start a new container by attaching STDIO and interactively and overriding the default command to run as 'bash' 
```sh
docker container run -it --name rajiv-nginx-2 nginx bash
```

### Enter an already running container and run command 'bash' to get a bash shell
> 'exec' will start an additional process in an existing container and will not affect the existing running       
> processes of that container. So, when you exit from the container, it will keep running
```sh
docker container exec -it rajiv-nginx-1 bash
```


