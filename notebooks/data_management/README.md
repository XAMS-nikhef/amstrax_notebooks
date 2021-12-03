# Datamanagement
j.angevaare@nikhef.nl
03.12.2021

## Datamanagement from stoomboot.
In this folder we have two usefull notebooks to :
 1. synchonize live data from the daq to stoomboot
 2. start mass production of raw records on stoomboot.

## Prerequisits
Please follow [setting up amstrax](https://amstrax.readthedocs.io/en/latest/setup.html#setting-up-amstrax) first. You might be able to start a notebook by doing the following:

Go to stoomboot, on the login node:
```bash
source deactivate
export PATH=/project/xenon/jorana/software/miniconda3/bin:$PATH
source activate /data/xenon/joranang/anaconda/envs/amstrax_2021
jupyter notebook --no-browser --port <some number between 10000-30000>
```
This should start jupyter on the login node (use with care! You should not do intensive jobs here!)

On your local host
```bash
ssh -f -N -L <some number between 10000-30000>:localhost:<some number between 10000-30000> <YOUR STOOMBOOT ALIAS>
```
For me `<YOUR STOOMBOOT ALIAS>` is `stbc` and this is set with a proxijump via the login node of nikhef.
