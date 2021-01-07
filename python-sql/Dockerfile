FROM ubuntu:18.04
LABEL maintainer="Ocean Protocol <devops@oceanprotocol.com>"

ARG VERSION

RUN apt-get update && \
    apt-get install --no-install-recommends -y \
    gcc \
    python3.6 \
    python3-pip \
    python3.6-dev \
    gettext-base

COPY . /tmp
WORKDIR /tnp

RUN python3.6 -m pip install setuptools
RUN python3.6 -m pip install -r /tmp/requirements.txt



