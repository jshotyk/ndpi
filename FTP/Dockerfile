FROM ubuntu:22.04

ENV HOME /root
# Define working directory.
WORKDIR /root

RUN apt-get update && apt-get upgrade -y &&\
    apt-get install -y \
        iproute2\
        vsftpd
RUN sed -i 's/#write_enable=YES/write_enable=YES/' /etc/vsftpd.conf\
&& sed -i 's/#chroot_local_user=YES/chroot_local_user=YES/' /etc/vsftpd.conf \
&& sed -i 's/#anonymous_enable=YES/anonymous_enable=YES/' /etc/vsftpd.conf
EXPOSE 20 21 40000-40100
