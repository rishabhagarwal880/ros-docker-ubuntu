# ROS_INDIGO-docker-ubuntu
The docker container to run Ubuntu 14.04 with ROS-indigo on Ubuntu 16.04. Please make sure that the docker CE is installed on the system and the docker deamon is running before building or running the container.


## Build the container Image
The image needs to be build everytime we make some changes in the Dockerfile. To build the image use the following command ''sudo ./build.sh $IMAGE_NAME(eg. ros-indigo)''. It might take some time for the first time to build the image but once you build the image you can use the same image.


## Run the image
To run the docker container use the following command ''sudo ./run.sh $IMAGE_NAME''. Once the image runs you will by default go to the docker. 

## Some key points
Make sure the X11-xserver-utils is installed in your system. To allow rosx running you need to allow xhost to receive from all the users by typing xhost + in the host terminal. Type ifconfig in the terminal and look for the ip-address assigned to docker. Add this IP on the xhost list by following command "xhost + $docker-ipaddress$". Since we are running docker as root we need to include root in xhost list by following command "xhost local:root"

