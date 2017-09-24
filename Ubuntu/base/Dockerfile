FROM ubuntu:16.04
MAINTAINER Jonathan Palomino <jonathan.palomino.vilca@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get dist-upgrade -y && \ 
apt-get install apt-utils --no-install-recommends -y && \ 
apt-get autoclean && apt-get autoremove --purge -y && \ 
rm -rf /var/lib/apt/lists/* /var/cache/apt/* /tmp/* /var/tmp/*
