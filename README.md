# singPyKeras
Singularity container for Python and Keras. Check releases for built images.

To build:
```
sudo singularity build pyKeras.simg Singularity
```

To use/test:
```
singularity exec --nv pyKeras.simg python3 kerasTest.py
```

To get into environment
```
singularity shell --nv pyKeras.simg
```

To get just an interactive python
```
singularity exec --nv pyKeras.simg python3
```
