- An [[Environment Managers | environment management]] platform for developing, shipping, and running applications in containers
- Ensures that the development environment is consistent across multiple devices and servers which might have different operating systems and installed packages 

#### Container
- A lightweight and portable [[Emulators and Virtual Machines#Virtual Machine | virtual machine]] like place that includes everything needed to run an application: code, runtime, dependencies
- They are isolated from each other and share the host OS kernel
  
#### Image
- Snapshot of a filesystem needed for an application to run
- The blueprint of containers

#### Docker Compose
- As applications grow it is common to separate parts of the application into distinct containers
	- For instance, it is common to put the [[Types of Databases | database]] server into a distinct container than the web app server
- This provides better scalability, resource optimization, fault isolation and portability
- Docker Compose allows developers to define and run multi-container Docker applications in a way that they can communicate

#### Docker Engine 
- Manages Docker containers on the host machine
- The Docker [[CLI]] is used to interact with the Docker Engine