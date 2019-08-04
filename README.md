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
- A text file with instructions to create image.
- By default the name is "Dockerfile"

## Steps to Create Docker
 - Step 1. Create Dockerfile
 - Step 2. Add instruction in Dockerfile --> https://docs.docker.com/engine/reference/builder/
 - Step 3. Build Dockerfile to create image
 - Step 4. Run image to create container


## Docker build commands
```
$ docker build .
$ docker build <file location>
$ docker build -t <tagename>:<version> .
```

### Docker Compose
Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration

### Using Compose is basically a three-step process:

Define your app’s environment with a Dockerfile so it can be reproduced anywhere.

Define the services that make up your app in docker-compose.yml so they can be run together in an isolated environment.

Run docker-compose up and Compose starts and runs your entire app.

### Docker Bare minimum file. docker-compose.yml
```
version: "3"

services: 

  web:
   image: nginx

  database:
   image: redis 
   
```

### Docker Compose Commands
```
$ docker-compose -v
$ docker-compose config //check if the config is valid/correct or not 
$ docker-compose up -d // -d for dettached mode
$ docker-compose down
$ docker-compose up -d --scale database=4 // to scale you instances. 
```
