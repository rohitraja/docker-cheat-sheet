# docker-cheat-sheet
Docker basic commands

### Docker images
```

$ docker pull <images name>:<tag name>
$ docker images
$ docker images -q
$ docker images -f "dangling=false" -q
$ docker run <image>
$ docker run -it <image>
$ docker rmi -f <image>
$ dockder inspect <image>
```

### Docker containers
Containers are the running instances of the images. 
```
$ docker ps
$ docker start <container Name/id>
$ docker stop <container Name/id>
$ docker pause <container Name/id>
$ docker unpuase <contianer Name/id>
$ docker top <container Name/id>
$ docker stats <container name/id>
$ docker stats
$ docker history <container name/id>

```

### Docker Architecture
<img src="linux-vs-docker-comparison-architecture-docker-components.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" />


### Docker File
