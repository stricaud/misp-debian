FROM debian:buster
MAINTAINER Sebastien Tricaud <sebastien@honeynet.org>
ARG DEBIAN_FRONTEND=noninteractive
RUN apt update -q
RUN apt -qy install net-tools iputils-ping vim emacs-nox
RUN apt -qy install curl sudo
RUN apt -qy install coreutils
RUN apt -qy install build-essential fakeroot devscripts dpkg-dev 
RUN apt -qy install pkg-config
RUN apt -qy install apache2-dev
RUN mkdir /opt/git/
WORKDIR /opt/git
RUN git clone https://github.com/misp/misp
WORKDIR /opt/git/misp
RUN git submodule init
RUN git submodule update

RUN mkdir /data
CMD ["sh", "-c", "tail -f /dev/null"]
