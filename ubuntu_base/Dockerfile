FROM ubuntu:16.04

ENV DEBIAN_FRONTEND=noninteractive
RUN sed -i s@archive.ubuntu.com@mirrors.ustc.edu.cn@g /etc/apt/sources.list
RUN apt-get update

# install basic libs
RUN apt-get -y install vim sudo
RUN apt-get -y remove x264 libx264-dev
RUN apt-get -y install build-essential checkinstall cmake pkg-config yasm
RUN apt-get -y install git gfortran
RUN apt-get -y install libjpeg8-dev libjasper-dev libpng12-dev
RUN apt-get -y install libtiff5-dev
RUN apt-get -y install libtiff-dev
RUN apt-get -y install libavcodec-dev libavformat-dev libswscale-dev libdc1394-22-dev
RUN apt-get -y install libxine2-dev libv4l-dev
RUN apt-get -y install libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev
RUN apt-get -y install libgtk2.0-dev libtbb-dev qt5-default
RUN apt-get -y install libatlas-base-dev
RUN apt-get -y install libfaac-dev libmp3lame-dev libtheora-dev
RUN apt-get -y install libvorbis-dev libxvidcore-dev
RUN apt-get -y install libopencore-amrnb-dev libopencore-amrwb-dev
RUN apt-get -y install libavresample-dev
RUN apt-get -y install x264 v4l-utils
RUN apt-get -y install libprotobuf-dev protobuf-compiler
RUN apt-get -y install libgoogle-glog-dev libgflags-dev
RUN apt-get -y install libgphoto2-dev libeigen3-dev libhdf5-dev doxygen

RUN apt-get -y install python3-dev python3-pip python3-venv

RUN apt-get -y install zsh

RUN groupadd -g 1000 ubuntu
RUN useradd -g 1000 -u 1000 -m -s /bin/zsh ubuntu
RUN usermod -aG sudo ubuntu
RUN echo "%sudo  ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/nopasswd

USER ubuntu:ubuntu
ENV HOME /home/ubuntu

WORKDIR ${HOME}

RUN pip3 install --upgrade pip
RUN pip3 install --upgrade setuptools
RUN pip3 install numpy 
RUN pip3 install matplotlib
RUN pip3 install opencv-python 

