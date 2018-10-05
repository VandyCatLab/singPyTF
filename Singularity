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
