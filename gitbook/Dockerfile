FROM ubuntu:xenial
MAINTAINER soulmachine <soulmachine@gmail.com>


RUN apt-get update -qy && apt-get -qy --no-install-recommends install \
    wget \
    build-essential \
 && apt-get clean \
 && apt-get autoremove \
 && rm -rf /var/lib/apt/lists/*


# see https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-16-04
RUN wget --no-check-certificate -qO- https://deb.nodesource.com/setup_6.x | bash \
 && apt-get -qy install nodejs \
 && npm install gitbook-cli -g \
 && apt-get clean \
 && apt-get autoremove \
 && rm -rf /var/lib/apt/lists/*


ENTRYPOINT ["/usr/bin/gitbook"]
