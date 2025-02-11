FROM ubuntu:22.04

RUN apt update && \
    apt install -y vim cmake clang gcc g++ python3 python3-pip git wget curl libnvidia-ml-dev

RUN wget https://go.dev/dl/go1.23.2.linux-amd64.tar.gz && \
    tar xvf go1.23.2.linux-amd64.tar.gz && \
    rm go1.23.2.linux-amd64.tar.gz && \
    echo "export PATH=$PATH:/go/bin" >> ~/.bashrc
