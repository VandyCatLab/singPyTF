# singPyKeras
Singularity container for Python and Keras. Check releases for built images.

To build:
```
sudo singularity build pyTF.sif Singularity
```

To use/test:
```
singularity exec --nv pyTF.sif python kerasTest.py
```

To get into environment
```
singularity shell --nv pyTF.sif
```

To get just an interactive python
```
singularity exec --nv pyTF.sif python
```
