FROM amazonlinux:latest
LABEL maintainer="noone@pairspaces.com"
LABEL base.name="NodeJS Base Image" \
      base.version="${VERSION}"

RUN dnf -y install gcc-c++ git gzip make shadow-utils tar
RUN dnf install https://rpm.nodesource.com/pub_18.x/nodistro/repo/nodesource-release-nodistro-1.noarch.rpm -y && \
    dnf install nodejs -y --setopt=nodesource-nodejs.module_hotfixes=1

RUN useradd -m -s /bin/bash pair
USER pair