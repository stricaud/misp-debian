FROM debian:buster

MAINTAINER Sebastien Tricaud <sebastien@honeynet.org>
ARG DEBIAN_FRONTEND=noninteractive
RUN apt update -q
RUN apt -qy install net-tools iputils-ping vim emacs-nox
RUN apt -qy install curl sudo
RUN apt -qy install coreutils
RUN apt -qy install build-essential fakeroot devscripts dpkg-dev 
RUN apt -qy install pkg-config
RUN apt -qy install ca-certificates python3 python3-setuptools python3-wheel composer mariadb-client openssl zip unzip moreutils php-pear libfuzzy-dev
RUN apt -qy install libapache2-mod-php7.3 php7.3 php7.3-cli php7.3-dev php7.3-json php7.3-xml php7.3-mysql php7.3-opcache php7.3-readline php7.3-mbstring php-redis php-gnupg php-gd
RUN apt -qy install supervisor debconf-utils
RUN apt -qy install python3-zmq python3-pip python3-redis
RUN apt -qy install rsyslog-gnutls
RUN apt -qy install php-mysql
ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf

RUN mkdir /data 
CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]

