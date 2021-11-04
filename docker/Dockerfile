FROM pman0214/pytorch_jupyterlab:1.9.0

ENV DEBIAN_FRONTEND=noninteractive
MAINTAINER Ryuichi YAMAMOTO <zryuichi@gmail.com>

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        curl \
        git \
        build-essential \
        libsamplerate0 \
        libsndfile1 \
        libhdf5-dev \
        pulseaudio \
        libasound2-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN pip install --no-cache-dir \
        ttslearn \
        simpleaudio

ENV LD_PRELOAD=/usr/lib/aarch64-linux-gnu/libgomp.so.1
