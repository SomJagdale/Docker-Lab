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

