Bootstrap: docker
From: ubuntu:16.04
IncludeCmd: yes

%environment
  CUDA_HOME=/usr/local/cuda
  export CUDA_HOME
  LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:${CUDA_HOME}/lib64
  export LD_LIBRARY_PATH
  PATH=${CUDA_HOME}/bin:${PATH}
  export PATH

%labels
Author Jason Chow
Version v0.01

%files
  libcudnn.deb
  cuda.deb

%post
apt update
apt install -y python3-dev python3-pip
pip3 install -U virtualenv
