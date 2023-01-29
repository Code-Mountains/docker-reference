# Getting Started 
docker run -d -p 80:80 --name docker-starter docker/getting-started

# View all Docker processes
docker ps -a

# Run Ubuntu docker image
docker run -it --name kubuntu ubuntu 

# Start a stopped container
docker start kubuntu

# Stop a running container
docker stop kubuntu

# Attach to a running container
docker attach kubuntu

# Start bash session in a running background container
docker exec -it docker-start /bin/sh

# Fetch Logs from a container
docker logs kubuntu

# Inspect container's running processes
docker top kubuntu

# Delete/Remove container
docker remove kubuntu

# Build Custom docker image (with Dockerfile on same folder as ./ )
docker build -t getting-started .  
(-t tag image with name 'getting-started')  
(. is to instruct docker to look for Dockerfile in this folder for building image)  

# Run the docker image built using this image above  
docker run -dp 3000:3000 --name todo-app getting-started  
(-d run in detached mode)  
(-p bind port 3000 on host to 3000 on container)  
(--name container name as todo-app)  
(getting-started is name of docker image that was built earlier)  

# Login to Docker Hub or any custom docker registry
docker login -u kdango

# Tag our custom docker image
docker tag getting-started kdango/getting-started  
(getting-started is source image)  
(kdango/getting-started is target image)  
(make sure kdango/getting-started repo is created on docker hub first, or in the custom docker registry)  

# Push our image to docker hub or custom docker registry
docker push kdango/getting-started  

# Create updated docker image from a running container
docker commit 28ed9a9fe253 getting-started-v2  
docker commit todo-app getting-started-v2  
(todo-app is the running container name or container id with latest changes from which to build the new docker image)  
(getting-started-v2 is name of new docker image)  

# Create new container from newly built docker image above  
docker run -dp 3001:3000 --name todo-app-v2 getting-started-v2

# Run commands on docker container
docker exec -it c-todo-app /bin/sh -c 'echo $HOSTNAME'  
(c-todo-app is container name)  
(/bin/sh is binary or executable to run)  
(-c 'echo $HOSTNAME' is the command to run on the shell)  
