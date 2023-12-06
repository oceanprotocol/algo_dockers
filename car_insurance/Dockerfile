FROM python:3.11

RUN apt-get update && \
    apt-get install --no-install-recommends -y \
    python3-tk \
    tk-dev \
    python3-pip \
    libagg-dev \
    libgl1-mesa-glx -y

RUN apt-get install 'ffmpeg'\
    'libsm6'\
    'libxext6' -y
    
COPY requirements.txt /tmp/
RUN pip install wheel
RUN pip install -r /tmp/requirements.txt