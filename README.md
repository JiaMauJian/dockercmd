
# kears in docker
 * https://qiita.com/niisan-tokyo/items/095ce51d366c3b24f229
 * https://hub.docker.com/r/gw000/keras/


# solving-docker-permission-denied-while-trying-to-connect-to-the-docker-daemon-socket/
sudo usermod -a -G docker$USER


# docker commnads
  * docker info
	* docker run hello-world
	* docker images
	* docker run -it xxx ( The combination of the -i and -t switches gives you interactive shell access into the container ) 
	* docker ps
	* docker kill $(docker ps -q)
	* exit
  
# docker run commnads (ex: docker run --rm -v `pwd`:/srv/ gw000/keras python learn.py)
	* https://docs.docker.com/engine/reference/commandline/run/#parent-command
	* --rm Automatically remove the container when it exits
	* --volume , -v Bind mount a volume
  
# gw000/keras-full (把/home/allen掛載到/srv，這樣子寫完的python檔案才不會隨時container下線而消失)
	*  docker run -v=/home/allen:/srv -d -p=6006:6006 -p=8888:8888 gw000/keras-full

# 用docker ps查CONTAINER  ID，用CONTAINER ID進去
	* docker exec -it fb08017a810d /bin/bash
