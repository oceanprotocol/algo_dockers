FROM python:3.8

RUN apt-get update && \
    apt-get install --no-install-recommends -y \
    python3-tk \
    tk-dev \
    python3-pip \
    libagg-dev
    
COPY requirements.txt /tmp/
RUN pip install wheel
RUN pip install -r /tmp/requirements.txt