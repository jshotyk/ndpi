# Choosing an operating system.
FROM ubuntu:22.10

ENV HOME /root
# Define working directory.
WORKDIR /root

RUN apt update && apt upgrade -y &&\
    apt install -y\
        #A set of utilities for managing network device parameters in the Linux kernel.
        iproute2\
        iputils-ping\
        #A cross-platform command-line utility that allows you to interact with many different servers.
        curl\
        #Libraries recommended by developers for nDPI work.
        gettext\
        flex\
        build-essential\
        bison\
        libtool\
        autoconf\
        automake\
        pkg-config\
        libpcap-dev\
        libjson-c-dev\
        libnuma-dev\
        libpcre2-dev\
        libmaxminddb-dev\
        librrd-dev\
        libtool\
        make

RUN curl -kL https://github.com/ntop/nDPI/archive/refs/tags/4.4.tar.gz | tar -xvz && \
    cd /root/nDPI-4.4 && \
    ./autogen.sh && \
    ./configure &&  \
    make && \
    make install