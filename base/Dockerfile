FROM debian:jessie

RUN apt-get update && apt-get install -y --no-install-recommends \
    apt-transport-https \
		pkg-config \
    bash \
		build-essential \
    ca-certificates \
    curl \
    git \
    groff \
    jq \
    netcat-openbsd \
    openssh-client \
    rsync \
    software-properties-common \
    tar \
    vim \
    wget \
    zip unzip \
    && rm -rf /var/cache/apk/* 

## key docker
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable" && apt-get update && apt-get install docker-ce -y

ADD docker.service /lib/systemd/system/docker.service