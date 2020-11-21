# How to Install Miniconda on Ubuntu 20.04

acticle

To install Miniconda on Ubuntu 20.04 from command line, it only takes 3 steps excluding creating and activating a conda environment.

## Download the latest shell script
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

## Make the miniconda installation script executable
chmod +x Miniconda3-latest-Linux-x86_64.sh

Run miniconda installation script
./Miniconda3-latest-Linux-x86_64.sh

## Create and activate an conda environment
To create a conda environment, run 

$ conda create -n newenv

You can also create the environment from a file like environment.yml, you can use use the conda env create -f command: conda env create -f environment.yml. The environment name will be the directory name.

## avoid conda to activate base environment

in your /home/***/.bashrc


source
https://varhowto.com/install-miniconda-ubuntu-20-04/

reference

https://www.youtube.com/watch?v=23aQdrS58e0&t=767s


