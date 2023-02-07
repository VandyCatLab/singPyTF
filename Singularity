Bootstrap: docker
From: tensorflow/tensorflow:2.11.0-gpu-jupyter
IncludeCmd: yes

%labels
Author Jason Chow
Version v2.00

%post
  # Install python and dependencies
  pip3 install --upgrade pip
  pip3 install tensorflow_hub pydub tensorflow_io
  
  apt-get update
  apt-get install -y ffmpeg
  
  