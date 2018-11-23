ARG UBUNTU_VERSION
FROM ubuntu:${UBUNTU_VERSION}

ARG CURRENT_TZ

RUN apt update && \
    DEBIAN_FRONTEND=noninteractive \
    apt install -yq --no-install-recommends \
        tzdata && \
    rm -rf /var/lib/apt/lists/* && \
    ln -fs /usr/share/zoneinfo/$CURRENT_TZ /etc/localtime
