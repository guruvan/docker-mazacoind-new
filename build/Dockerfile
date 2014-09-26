# version 1.4-1
# docker-version 0.9.1
FROM        phusion/baseimage:0.9.13
MAINTAINER  guruvan "guruvan@shastafareye.net"

# We use a bootstrap script to avoid having temporary cache files and build
# dependencies being committed and included into the docker image.
ADD         bootstrap.sh /tmp/
RUN         chmod +x /tmp/bootstrap.sh
RUN         /tmp/bootstrap.sh


ADD         mazacoin.conf /root/.mazacoin/
RUN         pass=`makepasswd -char 32` ;echo "rpcpassword=${pass}"  >> /root/.mazacoin/mazacoin.conf 
RUN         chmod 600 /root/.mazacoin/mazacoin.conf
ADD	    mazacoind.run /etc/service/mazacoind/run
RUN         chmod 700 /etc/service/mazacoind/run

EXPOSE      12832
EXPOSE      12835
EXPOSE      22
#ENTRYPOINT  [""]
CMD         ["/sbin/my_init"]
