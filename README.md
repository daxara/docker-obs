# docker-obs

A Docker image with [Open Broadcaster Software][obs] container to stream video content.

## Usage

#### Build Docker image

From the source file

	$ docker build --rm -t spoon4/docker-obs:latest .

or from [Docker Hub][dockerhub]

	$ docker pull spoon4/docker-obs

#### Start Open Broadcaster Software

With the start script after granted exec permission

	$ chmod a+x start.sh
	$ ./start.sh

or by setting a bash alias
	
	$ alias obs='docker run -ti --rm -e DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/home/obs/.Xauthority --device /dev/dri --net=host spoon4/docker-obs'

[obs]: https://obsproject.com
[dockerhub]: https://hub.docker.com/r/spoon4/docker-obs