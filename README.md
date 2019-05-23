# pytorch-singularity
A singularity and docker container to run pytorch in a HPC environment

Build the image/container with

```
sudo singularity build --writable dtorch.img dtorch.txt
```

And execute with somethign like this:
```
singularity exec -B `pwd` --nv dtorch.img python `pwd`/testGPU.py
```

See the \*.pbs file for more way that we interact with this image on the command line, and specifically in a "headless/batch" HPC environemnt.
