vim
---

unofficial vim in singularity container, contain python extension


Python support in vim.
eg inside vim, be able to run:

:python import sys; print(sys.version)

more info at:
https://realpython.com/vim-and-python-a-match-made-in-heaven/


Cluster has a very tiny version of vi.
This version of vi from Centos 7/8 has python2.
check per vim --version



Build
-----

sudo singularity build --sandbox ./pyvim.sif Singularity 2>&1 | tee singularity_build.log 

