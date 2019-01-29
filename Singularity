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
  # Install python and dependencies
  apt-get update
  apt-get install -y \
    python3-dev \
    python3-pip \
    locales \
    language-pack-en

  pip3 install -t /usr/lib/python3/dist-packages/ --upgrade virtualenv

  # Install tensorflow and keras
  pip3 install -t /usr/lib/python3/dist-packages/ --upgrade tensorflow-gpu
  pip3 install -t /usr/lib/python3/dist-packages/ --upgrade keras

  # Install pillow
  pip3 install -t /usr/lib/python3/dist_packages/ --upgrade pillow
  
  # Cuda support
  apt-get install -y linux-headers-$(uname -r)
  dpkg -i cuda.deb
  apt-key add /var/cuda-repo-9-0-local/7fa2af80.pub
  apt-get update
  apt-get install -y cuda

  # cudnn
  dpkg -i libcudnn.deb
  apt-get update
  apt-get install -y libcupti-dev

  # ACCRE binding points
  mkdir /scratch /data /gpfs22 /gpfs23
