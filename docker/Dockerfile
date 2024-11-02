FROM ubuntu:22.04
LABEL author="Radu Daia <radu.daia@pm.me>"
LABEL version="v1.0.0"

RUN apt-get update -y
RUN TZ=Etc/UTC DEBIAN_FRONTEND=noninteractive \
    apt-get -y install gawk wget git diffstat unzip texinfo gcc build-essential \
                        chrpath socat cpio python3 python3-pip python3-pexpect \
                        xz-utils debianutils iputils-ping python3-git python3-jinja2 \
                        libegl1-mesa libsdl1.2-dev python3-subunit mesa-common-dev \
                        zstd liblz4-tool file locales libacl1
RUN locale-gen en_US.UTF-8
RUN useradd -ms /bin/bash yocto
USER yocto
WORKDIR /home/yocto