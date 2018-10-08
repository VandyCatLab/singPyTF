# singPyKeras
Singularity container for Python and Keras

To build:
```
sudo singularity build pyKeras.simg Singularity
```

To use/test:
```
singularity exec pyKeras.simg python3 -i kerasTest.py
```

To get into environment
```
singularity shell pyKeras.simg
```

To get just an interactive python
```
singularity exec pyKeras.simg python3
```
