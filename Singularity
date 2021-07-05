Bootstrap: docker
From: tensorflow/tensorflow:2.3.1-gpu-jupyter
IncludeCmd: yes

%labels
Author Jason Chow
Author Sam Lee
Version v0.04

%post
  apt-get update

  # Jupyter and important libraries
  pip install scipy tensorflow-addons pandas
  # Text editors and git
  apt -y install nano git

  
  
