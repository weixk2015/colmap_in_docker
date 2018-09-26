# colmap-in-docker

This github repo aims to help you build a docker image with colmap residing in.

Prerequites: make sure [docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/) and [nvidia-docker2](https://github.com/NVIDIA/nvidia-docker) are installed on your system. And also make sure that the nvidia driver installed on your system is compatible with cuda-8.0; otherwise you need to modify the base image in the Dockerfile.

The workflow is as below:
* switch to the directory 'colmap_in_docker' after you git-clone the repo
* run './build_colmap.sh'; this build a docker image called 'kai46/colmap:latest' on your local machine
* run './run_colmap.sh'; this will launch a container and lead you to the bash; the script takes care of mapping host user id, and mounting host volume into the newly launched container
* enjoy

Feel free to modify the Dockerfile and the two handy scripts yourlf. Inside the 'reference' folder, there are two Dockerfiles provided by NVIDIA. I was referencing them to figure out how to install CUDA.
 
