# Docker-Lab

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

docker container [action]
  action
  attach      Attach local standard input, output, and error streams to a running container
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  inspect     Display detailed information on one or more containers
  kill        Kill one or more running containers
  logs        Fetch the logs of a container
  ls          List containers
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  prune       Remove all stopped containers
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  run         Run a command in a new container
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  wait        Block until one or more containers stop, then print their exit codes


