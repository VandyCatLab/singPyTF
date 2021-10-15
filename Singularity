Bootstrap: docker
From: tensorflow/tensorflow:2.5.0-gpu-jupyter
IncludeCmd: yes

%labels
Author Jason Chow
Author Sam Lee
Version v0.04

%environment
  export LD_LIBRARY_PATH=/opt/intel/compilers_and_libraries_2020/linux/mkl/lib/intel64/:/opt/intel/compilers_and_libraries_2020/linux/lib/intel64:$LD_LIBRARY_PATH

%post
  apt-get update
  apt-get -y install wget nano gfortran

  # Get Intel MKL
  wget https://apt.repos.intel.com/intel-gpg-keys/GPG-PUB-KEY-INTEL-SW-PRODUCTS-2019.PUB
  apt-key add GPG-PUB-KEY-INTEL-SW-PRODUCTS-2019.PUB
  rm GPG-PUB-KEY-INTEL-SW-PRODUCTS-2019.PUB
  wget https://apt.repos.intel.com/setup/intelproducts.list -O /etc/apt/sources.list.d/intelproducts.list
  apt-get update

  apt-get -y install intel-mkl-2020.0-088

  wget https://raw.githubusercontent.com/VandyCatLab/singPyKeras/master/.numpy-site.cfg -O ~/.numpy-site.cfg

  # Update pip
  pip install --upgrade pip

  # Install easy stuff and dependencies for python 
  pip install tensorflow-addons tensorflow-datasets tensorflow-hub pandas numba Cython pythran

  # Build numpy and scipy from source for mkl support
  pip install numpy==1.19.2 scipy --no-binary numpy,scipy --force-reinstall
  


  
  
