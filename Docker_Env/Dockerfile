FROM ubuntu:20.04

COPY gcc-arm-10.3-2021.07-x86_64-aarch64-none-linux-gnu.tar.gz /opt/

RUN apt-get update 
RUN apt-get install openssh-server -y
RUN apt-get install sudo time ssh vim fakeroot -y 
RUN apt-get install make cmake gcc-multilib g++-multilib device-tree-compiler -y 
RUN apt-get install make-guile gcc -y 
RUN apt-get install bison flex bc diffstat binfmt-support qemu-user-static -y 
RUN apt-get install libncurses5-dev libncursesw5-dev python3 python-is-python3 g++ -y 
RUN apt-get install libssl-dev kmod squashfs-tools liblz4-tool expect patchelf chrpath texinfo -y
RUN apt-get install language-pack-en language-pack-en-base locales -y 
RUN mkdir -p /opt/toolchain 
RUN tar -xzvf /opt/gcc-arm-10.3-2021.07-x86_64-aarch64-none-linux-gnu.tar.gz -C /opt/toolchain/ 
RUN apt-get install build-essential patch perl cpio unzip rsync cvs git -y 
RUN apt-get install debootstrap qemu-user-static debian-archive-keyring -y 
RUN apt-get install meson live-build libgmp-dev libmpc-dev libicu-dev bsdmainutils python2 -y 

ENV PATH="$PATH:/opt/toolchain/gcc-arm-10.3-2021.07-x86_64-aarch64-none-linux-gnu/bin"
