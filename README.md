# Debian Image Container

Considering that the "debian-docker" repository, an excellent work by Jonathan Dowland,  
has become deprecated and I prefer to use PODMAN instead of Docker and I want to use my  
own Debian images, I chose to do some adjustments to the original work.  

I recommend reading the [original README content](https://github.com/jmtd/debian-docker/blob/master/README.md), which contains the indication for Joey Hess's  
pertinent work, as well as reading the Debian Wiki page that motivated my research on Docker and  
took me to PODMAN.

All credits belong to Jonathan Dowland to whom I publicly thank.

[Wiki Debian/Podman](https://wiki.debian.org/Podman)  

[Wiki Debian/Docker](https://wiki.debian.org/Docker), that makes the alert: "Docker group membership is more dangerous than sudo".  

[what does docker.io run -it debian sh run?](https://joeyh.name/blog/entry/docker_run_debian/), by 
Joey Hess, which recommends <q>only trust docker images you build yourself</q>.  

# Getting started  

To build your own images run  

----
>sudo apt-get install git make debootstrap  

>git clone https://github.com/fernandolcouto/deb-img-ctnr.git  

>cd deb-img-ctnr/  

>sudo make release=buster prefix=fernandolcouto arch=amd64 mirror=http://httpredir.debian.org/debian/  

----

All the arguments above are optional.  

The values in the example above are the defaults.  

The resulting image would be tagged fernandolcouto/debian:buster-amd64

