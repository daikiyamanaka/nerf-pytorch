FROM nvidia/cuda:11.0.3-devel-ubuntu20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip \
    libgl1-mesa-dev\
    libopencv-dev

COPY requirements.txt requirements.txt

RUN pip3 install torch==1.9.0+cu111 torchvision==0.10.0+cu111 torchaudio==0.9.0 -f https://download.pytorch.org/whl/torch_stable.html

RUN pip3 install -r requirements.txt
