docker-mazacoind-new
====================

docker build based on new mazacoin 

This docker will build a mazacoind from official mazacoin github repo. 
Baseimage uses is phusion/baseimage - no modifications. This will apt-get all the necessary tools to build the latest version of mazacoind, compile mazacoind & install.

To build yourself, 

<code>git clone https://github.com/ShastaFarEye/docker-mazacoind-new<
cd docker-mazacoind-new/build
make</code>

