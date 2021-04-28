# docker build -t ctf-image . --platform linux/amd64
# docker run --platform linux/amd64 --rm --volume $PWD:/pwd --cap-add=SYS_PTRACE --security-opt seccomp=unconfined --detach --name ctf --interactive ctf-image
# docker exec -it ctf /bin/bash

FROM ubuntu:18.04
ENV LC_CTYPE C.UTF-8
ENV DEBIAN_FRONTEND=noninteractive
RUN dpkg --add-architecture i386
RUN apt-get update
RUN apt-get install vim \
	git \
	curl \
	wget \
	make \
	gcc \
	gdb \
	tree \
	tmux \
	build-essential \
	gcc-multilib \
	gdb-multiarch \
	libc6:i386 \
	python3 \
	python3-pip \
	python3-dev \
	-y
