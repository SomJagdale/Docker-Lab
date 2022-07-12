  974  docker image save ntr:pg --file ntrtest
  975  docker image save ntr:pg -o ntrtest
  977  docker image load -i ntrtest
  979  docker image build --tag java:v1 -f Dockerfile_java .
  985  docker image tag java:v2 docker.io/somanath89/java:v2
  986  docker image tag java:v2 docker.io/somanath89/java:v1
  987  docker image tag java:v1 docker.io/somanath89/java:v1
  989  docker login
  990  docker image push somanath89/java:v1
  991  docker image pull alpine
  992  docker images
  993  docker image pull alpine                   latest    e66264b9
  994  docker image pull somanath89/java:v1
  995  docker images
  998  ls 821406/ns/net
  999  cd /proc/873931/ns/
 1008  docker container stop ntrcontainer2
 1009  docker ps
 1010  docker container start ntrcontainer2
 1011  docker ps
 1012  docker container pause ntrcontainer2
 1013  docker ps
 1014  docker container uspause ntrcontainer2
 1015  docker container unpause ntrcontainer2
 1016  docker ps
 1017  docker container kill ntrcontainer2
 1018  docker ps
 1019  docker container create ntrcontainer2
 1020  docker container create
 1021  docker container create --name ntrcont2 ntr:pg
 1022  docker ps
 1023  docker container start ntrcont2
 1024  docker ps
 1025  docker container run -d --name ntrcont3 ntr:pg
 1026  docker container run -d --name ntrcont4 ntr:pg
 1027  docker ps
 1028  dcoker container exec -it ntrcont4 sh
 1029  docker container exec -it ntrcont4 sh
 1030  docker container exec -it ntrcont3 sh
 1031  docker container exec -it ntrcont2 sh
 1032  docker ps
 1033  docker image
 1034  docker images
 1035  docker container run --name javac1 java:v1 ping google.com
 1036  docker container run --name javac2 java:v1 ping google.com
 1037* docker container run --name javacont1 java:v1 ping google.com
 1038  ls
 1039  docker images
 1040  docker container run --name alpinc1 alpine:latest ping google.com
 1041  docker container run -d --name alpinc1 alpine:latest ping google.com
 1042  docker container run -d --name alpinc2 alpine:latest ping google.com
 1043  docker ls
 1044  docker ps
 1045  docker container exec -it alpinc2 sh
 1046  docker container run -d --name ntrcont5 ntr:pg ping google.com
 1047  docker container attach 4cc4d1e380a7b1a5f4586de2c2b277896b85b8ba21e5ac1a6ff4cf84f5786562
 1048  docker ps
 1049  docker container run -d --name ntrcont6 ntr:pg ping google.com
 1050  docker ps
