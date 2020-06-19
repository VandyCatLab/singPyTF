# singPyKeras
Singularity container for Python and Keras. Check releases for built images.

To build:
```
sudo singularity build pyKeras.sif Singularity
```

To use/test:
```
singularity exec --nv pyKeras.sif python kerasTest.py
```

To get into environment
```
singularity shell --nv pyKeras.sif
```

To get just an interactive python
```
singularity exec --nv pyKeras.sif python
```
