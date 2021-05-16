FROM scratch
LABEL maintainer="fernandolcouto<fernandolcouto@gmail.com>"
ADD sid-chroot.tar /
RUN apt-get update \
	&& apt-get -y upgrade \
	&& apt-get -y autoremove \
	&& apt-get clean \
	&& find /var/lib/apt/lists -type f -delete
CMD ["/bin/bash"]
