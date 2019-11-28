FROM debian:8-slim

RUN apt update && apt install -y \
    wget \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /root/s3git

RUN wget -q -O s3git https://github.com/s3git/s3git/releases/download/v0.9.2/s3git-linux-amd64
RUN chmod +x s3git
ENV PATH=$PATH:/root/s3git/


RUN s3git

ENTRYPOINT [ "s3git" ]