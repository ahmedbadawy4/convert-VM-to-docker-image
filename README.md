# convert-VM-to-docker-image
convert VM to docker image

form  https://docs.docker.com/engine/userguide/eng-image/baseimages/ 

apt-get install -y debootstrap

 cat /etc/lsb-release # to get the release name of the distribution of Linux you are running which is a trusty release of Ubuntu

 debootstrap trusty <unique_name> > /dev/null

 tar -C <unique_name> -c . | sudo docker import - <unique_name>

 docker images
