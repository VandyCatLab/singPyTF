Bootstrap: docker
From: tensorflow/tensorflow:2.2.0-gpu
IncludeCmd: yes

%labels
Author Jason Chow
Author Sam Lee
Version v0.03

%post
  # Jupyter
  apt install python3-notebook jupyter jupyter-core python-ipykernel  
  # Important Python libraries
  pip install matplotlib scikit-learn pandas
  # Text editors
  apt install neovim nano

  
  
