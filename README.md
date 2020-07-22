# Docker
Working with Docker (Main commands)
___

# PREPARING (Ubuntu x86_64 / amd64)
___
```sudo apt-get update```

```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```
    
```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```

```sudo apt-key fingerprint 0EBFCD88```

# INSTALL DOCKER ENGINE
___
```sudo apt-get update```

```sudo apt-get install docker-ce docker-ce-cli containerd.io```

# CHECK
___
```docker -v```

```sudo systemctl status docker```

# MAIN COMMANDS
___

```docker  ps -a  #list all containers```

```docker images  #list all images```

```docker search [container_name] #search by container_name```

```docker build -t [container_name] . #build image based on Dockerfile in current directory```

```docker run -it  -p 1234:80  [container_name]:latest```

```docker run -d -p  1234:80  [container_name]:latest```

```docker rm [container_id] # delete container```

```docker rmi [image_id] # delete image```

```docker exec -ti [container_id] sh```

 ```docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' [container_id] #get ip for conteiner```

