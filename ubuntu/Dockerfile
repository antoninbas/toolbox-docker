ARG UBUNTU_VERSION=22.04
FROM ubuntu:${UBUNTU_VERSION}
LABEL maintainer="Antonin Bas <antonin.bas@gmail.com>"
LABEL description="A Docker image with useful tools (for networking) based on Ubuntu"

# Keep it in lexicographic order
ENV DEPS arping \
         curl \
         dnsutils \
         ethtool \
         iperf \
         iproute2 \
         iputils-ping \
         ncat \
         nmap \
         socat \
         tcpdump \
         telnet \
         traceroute \
         wget

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends $DEPS && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

CMD ["sleep", "infinity"]
