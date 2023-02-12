Bootstrap: docker

From: tensorflow/tensorflow:2.11.0-gpu-jupyter

IncludeCmd: yes

%labels
Author Jason Chow
Version v2.00

%post
  apt-get update
  apt-get -y install wget nano ffmpeg

  # Update pip
  pip install --upgrade pip

  # Install easy stuff and dependencies for python 
  pip install tensorflow-addons==0.19.0 \
    tensorflow-datasets==4.8.2 \
    tensorflow-hub==0.12.0 \
    tensorflow-io==0.30.0 \
    pydub==0.25.1 \
    pandas==1.5.3 \
    numba==0.56.4 \
    scikit-learn==1.2.1 \
    matplotlib==3.6.3 \
    seaborn==0.12.2 \
    opencv-python==4.7.0.68 \
    torch==1.13.1 \
    torchvision==0.14.1 \
    timm==0.6.12 \
    transformers==4.26.1 \
    pretrainedmodels==0.7.4


  
