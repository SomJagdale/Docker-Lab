  677  docker ps
  678  docker container -itd --name test1 alpine
  679  docker container run -itd --name test1 alpine
  680  docker run -itd --name test1 alpine
  681  docker run -itd --name test2 alpine
  682  docker inspect 2a7b742d308fe32eccbd6e7238147eeab6436d1340045ad5cac7e15fefd8d8ef
  683  docker inspect 2a7b742d308fe32eccbd6e7238147eeab6436d1340045ad5cac7e15fefd8d8ef | less
  684  docker network ls
  685  docker inspect test2 --format='{{.NetworkSettings.IPAddress}}'
  686  docker inspect test1 --format='{{.NetworkSettings.IPAddress}}'
  687  docker exect -it test1 sh
  688  docker exec -it test1 sh
  689  docker network create alpine-net
  690  docker network ls
  691  docker inspect alpine-net
  692  docker run -itd alpinenetc1 --network alpine-net alpine
  693  docker container run -itd alpinenetc1 --network alpine-net alpine
  694  docker container run -itd --name alpinenetc1 --network alpine-net alpine
  695  docker container run -itd --name alpinenetc2 --network alpine-net alpine
  696  docker inspect alpinenetc1 --format='{{.NetworkSettings.IPAddress}}'
  697  docker inspect alpinenetc2 --format='{{.NetworkSettings.IPAddress}}'
  698  docker inspect alpinenetc1 | less
  699  docker inspect alpinenetc2 | less
  700  docker exec -it alpinenetc1 sh
  701  docker network ls
  702  docker container stop alpinenetc1
  703  docker container run -itd --name alpinenetc1 --network alpine-net alpine
  704  docker container start alpinenetc1
  705  docker inspect alpinenetc1
  706  docker rm alpinenetc1
  707  docker rm -f alpinenetc1
  708  docker rm alpinenetc1
  709  docker container run -itd --name alpinenetc1 --network alpine-net alpine
  710  docker inspect alpinenetc1
  711  docker container run -itd --name alpinenetc3 --network alpine-net alpine
  712  docker inspect alpinenetc3
  713  docker rm alpinenetc1
  714  docker rm -f alpinenetc1
  715  docker rm -f alpinenetc3
  716  docker container run -itd --name alpinenetc3 --network alpine-net alpine
  717  docker inspect alpinenetc3
  718  docker network create ntr-subnet --subnet 192.168.100.0/24 --gateway 192.168.100.1
  719  docker network ls
  720  docker network rm ntr-net ntr-net1 ntr-net3
  721  docker network rm -f ntr-net ntr-net1 ntr-net3
  722  docker  rm -f ntr-net ntr-net1 ntr-net3
  723  docker network create ntr-subnet --subnet 192.168.100.0/24 --gateway 192.168.100.1
  724  docker network create ntr-subnet --subnet 192.169.100.0/24 --gateway 192.168.100.1
  725  docker network create ntr-subnet --subnet 192.169.100.0/24 --gateway 192.169.100.1
  726  docker network ls
  727  docker run -itd --name netcont1 --ip 192.169.100.10 alpine
  728  docker inspect 7dc9f6137c565b8693721b7c39de448294bace5b35cfdbc2bb5d6149f724dee2
  729  docker run -itd --name netcont2 --network ntr-subnet --ip 192.169.100.10 alpine
  730  docker inspect b2c17afd3cd066bff57c29c59539cb2523fe1cff5da48aa4b0e4ae16d7659850
  731  docker run -itd --name netcont3 --network ntr-subnet --ip 192.169.100.10 alpine
  732  docker run -itd --name netcont3 --network ntr-subnet
  733  docker run -itd --name netcont4 --network ntr-subnet
  734  docker run -itd --name netcont4 --network ntr-subnet alpine
  735  docker inspect 9e40a7c11e33689b7373cf837f2e724742f3b2f25512268ffced9c0b27f091bb
  736  docker run -itd --name nginxc --p 1234:80 nginx
  737  docker run -itd --name nginxc -p 1234:80 nginx
  738  docker run -itd --name nginxc1 -p 1234:80 nginx
  739  docker run -itd --name nginxc2 -p 1224:80 nginx
  740  docker exec -it 480bef49cc3bc6d478cfe353c970c54987fcda86671f1c98ac9f8d83c20d815c sh
  741  netstat -tnulp | grep 1224
  742  docker run -itd --name nginxc5 -p 1225:80 nginx
  743  history
  744  netstat -tunulp | grep 16246
  745  docker ps
  746  netstat -tunulp | ls
  747  netstat -tunulp | less
  748  sudo kubectl run nginx --image=nginx -n default
  749  docker run -itd --name ngnxc1 nginx
  750  netstat -tunulp | less
  751  docker run -itd --name ngnxc2 --port 1234:80 nginx
  752  docker run -itd --name ngnxc2 -p 1234:80 nginx
