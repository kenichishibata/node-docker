# Docker Images

Docker images repository to make prebuilt environment using centos base and then built using osx docker toolkit

## Usage

1. Install docker (mac) [https://docs.docker.com/engine/installation/mac/](here)

2. Open docker quickstart terminal and then run **docker version** to check if docker works properly

3. (optional) _To check if docker daemon runs **docker run hello-world**_ (if it does not work retart terminal or iterm whichever you use)

4. Clone this repo in your local machine

5. Go to the desired image and then run **docker build -t (image name):(version|latest) .**

6. Run **docker images** to see if the docker image was built properly

7. Run **docker run -it (image name):(version|latest)**

8. To access the running machine **docker run -it (image name):(version|latest) bash**  
