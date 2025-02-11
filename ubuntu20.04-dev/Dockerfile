FROM ubuntu:20.04

ENV TZ=Asia/Shanghai \
    DEBIAN_FRONTEND=noninteractive

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone

RUN apt update
RUN apt install -y tzdata
RUN apt install -y vim cmake clang gcc g++ python3 python3-pip git wget curl libnvidia-ml-dev

RUN wget https://go.dev/dl/go1.23.2.linux-amd64.tar.gz && \
    tar xvf go1.23.2.linux-amd64.tar.gz && \
    rm go1.23.2.linux-amd64.tar.gz && \
    echo "export PATH=$PATH:/go/bin" >> ~/.bashrc

RUN apt install -y gnupg2 software-properties-common
RUN wget -O - https://apt.kitware.com/keys/kitware-archive-latest.asc 2>/dev/null | apt-key add -
RUN apt-add-repository "deb https://apt.kitware.com/ubuntu/ focal-rc main"
RUN apt update && \
    apt remove -y cmake && \
    apt install -y cmake
