ARG UBUNTU_VERSION=20.04
FROM ubuntu:${UBUNTU_VERSION}
LABEL maintainer="Antonin Bas <antonin.bas@gmail.com>"
LABEL description="A Docker image with useful tools (for networking) based on Ubuntu"

ENV DEBIAN_FRONTEND=noninteractive

# Keep it in lexicographic order
ENV DEPS arping \
         curl \
         dnsutils \
         ethtool \
         iperf \
         iproute2 \
         iputils-ping \
         nmap \
         tcpdump \
         telnet \
         traceroute \
         wget

RUN apt-get update && \
    apt-get install -y --no-install-recommends $DEPS && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
