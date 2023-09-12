FROM debian:bullseye

RUN dpkg --add-architecture arm64 && \
    apt-get update && \
    apt-get full-upgrade --no-install-recommends -y \
        build-essential crossbuild-essential-arm64 binutils-aarch64-linux-gnu git \
        debhelper devscripts lintian wget tar gzip && \
    adduser --gecos runner --disabled-password runner && \
    rm -rf /var/lib/apt/lists/*
