
# Docker-Lab
Docker Training Day 1

////////////////////////////////////////////////////////////////////////////////////////
1. VirtualBox/VMware/hyper-v Instllation - Ask IT team to install it on your laptop

2. Virtual image and repository
	http://kb.roamware.com/repo/isos/

3. Docker Instllation
   a. Docker repo(yum/apt/dnf)
		sudo yum install -y yum-utils
		sudo yum-config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
	
   b. Installing Docker
		sudo yum install docker-ce docker-ce-cli containerd.io docker-compose-plugin

4. Run Docker Engine
		sudo systemctl start docker
////////////////////////////////////////////////////////////////////////////////////////////			

1. Docker Image
	- Application along with its dependencies(environment and libraries) bundled together.
	  Encapsulation of the application and its dependencies.
	  application binary, .so binaries, configuration files, scripts and os level enviroment-ex. glibc(parent image)	

    - Container is instance of an image.	
	  Image is like template/blue-print from which we can create many containers.
	  Container is image in running state.



2. Show Diagram
	parent image	
		Parent image - This base image is basically an OS without kernel but has only userland software
		based on the different linux distributions.

	glibc - it is an API to call kernel level function like open, close, read, write or we can say wrapper on kernel function 
	       (this api specification changes according to os distributions)

3. Docker registry 
	A Docker registry is a repository for Docker images.
	dockerhub,Azure Container Registry,Google Container Registry,Github Container Registry)
    Show website 
	
3. Dockerfile

4. Docker image layers
	Each layer is an image itself, just one without a human-assigned tag. They have auto-generated IDs though.
    Each instruction in a Dockerfile results in a layer.
	Layers are used to avoid transferring redundant information and skip build steps which have not changed.	


Docker command reference(Docker has two main object or entity ie image and container)Solomon Hykes in 2013
https://docs.docker.com/engine/reference/commandline/cli/

	docker build .
	docker run file_name
	docker inspect _ID

or 
https://docs.docker.com/engine/reference/commandline/image/

	docker image build .
	docker container run _id
	docker image inspect _id
	docker container inspect _id		
		
4. Operations on the image
      
   docker images
   
   docker image build --tag ntr:pg .
   
   docker image inspect ntr:pg
   
   #reason why list of images and sha256 is different
   /var/lib/docker/image/overlay2/imagedb/content/sha256 
   
   #tagging
   docker image build --tag java:v1 -f Dockerfile_java .
   
   #pull push
   docker image tag java:v1 docker.io/somanath89/java:v1
   docker login
   docker push somanath89/java:v1
   
   #rmoving
   docker image rm somanath89/java:v1
   
   #pulling uploaded image
   docker pull somanath89/java:v1
   
   #reason why list of images and sha256 is different
   /var/lib/docker/image/overlay2/imagedb/content/sha256 
   
   #sharing to qe
   docker image save ntr:pg -o ntr80_pg
   
   #loading to qe setup
   docker image load -i ntr80_pg
   
   docker image rm -f 918732310e3c 23e09b76c8cd 127262e59d08
   to delete all the images
   docker image rm -f $(docker images -aq)
   
   docker container rm $(docker ps -aq)

  build       Build an image from a Dockerfile
  history     Show the history of an image
  import      Import the contents from a tarball to create a filesystem image
  inspect     Display detailed information on one or more images
  load        Load an image from a tar archive or STDIN
  ls          List images
  prune       Remove unused images
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rm          Remove one or more images
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE


Commands required to build the images
docker images 
docker image build
docker image inspect
docker image pull
docker image push 
docker image rm 
docker image tag 
docker image load 
docker image import 
docker image save

docker images 

docker image build .

docker image rm 9ab9539d5cc4

docker image build --tag pingImg:v1 .

docker images build --tag pingImag:v1

docker images build --tag pingImage:v2

docker image inspect 9ab9539d5cc4/imagename:v1

docker image  pull  docker.io/somanath89/somshimage:v1

docker image  tag couchbase:v1 docker.io/somanath89/couchbasereg:v1

sudo chmod 666 /var/run/docker.sock

docker image login

docker image push docker.io/somanath89/couchbasereg:v1


Docker Container

docker ps 

docker run -it imagename

docker exec -it container_id sh

docker inspect container_id

docker stop container_id

docker rm container_id

docker container logs container_id 

docker container [action]
  
