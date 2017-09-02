FROM centos:latest
MAINTAINER Jonathan Palomino <jonathan.palomino.vilca@gmail.com>

# get updates via yum
RUN yum -y upgrade && \
    yum -y update && \
    yum -y install wget unzip findutils && \
    yum clean all