FROM ubuntu:14.04
MAINTAINER Adam Stegman <astegman@gmail.com>

RUN apt-get -y update

RUN locale-gen en_US.UTF-8
RUN dpkg-reconfigure locales
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

# Install ChefDK
RUN apt-get -y install wget
RUN cd /tmp; \
    wget https://opscode-omnibus-packages.s3.amazonaws.com/ubuntu/12.04/x86_64/chefdk_0.6.2-1_amd64.deb; \
    dpkg -i chefdk_0.6.2-1_amd64.deb

# Clean up the image
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
