- An [[Environment Managers | environment management]] platform for developing, shipping, and running applications in containers
- Ensures that the development environment is consistent across multiple devices and servers which might have different operating systems and installed packages 

#### Image
- Snapshot of a filesystem needed for an application to run
- The blueprint of containers

#### Container
- An isolated and lightweight execution environment ([[Emulators and Virtual Machines#Virtual Machine | virtual machine]] like place) for an application
- Contains everything needed to run an application: code, runtime, dependencies, configurations
- Shares the host OS kernel

#### Docker Compose
- As applications grow it is common to separate parts of the application into distinct containers
	- For instance, it is common to put the [[Types of Databases | database]] server into a distinct container than the web app server
- This provides better scalability, resource optimization, fault isolation and portability
- Docker Compose allows developers to define and run multi-container Docker applications in a way that they can communicate

#### Docker Engine 
- Manages Docker containers on the host machine
- The Docker [[CLI]] is used to interact with the Docker Engine
  
#### Commands

- `docker build -t image_name:tag` -> Create Image
- `docker rmi image_id` -> Remove Image
- `docker pull image_id` -> Pull an Image From Docker Hub
- `docker images` -> List Images

- `docker run image_id` -> Start a Container
- `docker stop container_id` -> Stop a Running Container
- `docker rm container_id` -> Remove a Container
- `docker inspect container_id` -> Inspect a Container
- `docker ps` -> List Running Containers
- `docker ps -a` -> List All Containers