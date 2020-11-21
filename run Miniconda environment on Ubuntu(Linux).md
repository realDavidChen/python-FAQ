# How to run Miniconda environment on Ubuntu 20.04

acticle

To install Miniconda on Ubuntu 20.04 from command line, it only takes 3 steps excluding creating and activating a conda environment.

## Download the latest shell script
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

## Make the miniconda installation script executable
chmod +x Miniconda3-latest-Linux-x86_64.sh

Run miniconda installation script
./Miniconda3-latest-Linux-x86_64.sh

## conda activate and activate or deactivate
$ conda activate 

you can see "base" in the line front
or you can deactivate conda

$ conda deactivate

"base" word disable



## Create and activate an conda environment
To create a conda environment, run 

$ conda create -n newenv

## create environment and into news environment example

$ conda create --name kivy python=3.7

check even list

$ conda env list

into news create env

$ conda activate kivy

or 

$ source.activate kivy

you will see the front world: (kivy) $ ... like this.  

## then you into special environment, you can using pip3 install application like normal, but the application will run in the special environment. not on the global env.

(kivy)$ pip3 search kivy

you can get kivy related version packages on the list,then, select what you want version. install the special version into 'kivy' project environment,like this:

(kivy)$ pip3 install kivy==1.11.1

and finally, kivy 1.11.1 version and python3.7 version  will install to new environment => kivy 

## how to use conda environment in VS studio editor

creat a python format file like " main.py ", open the file, in VS studio  button will show you related python version, python3.8 or other version, click version, and then select you customize conda environment version like : python 3.7 or another








## avoid conda to activate base environment

in your /home/***/.bashrc


source
https://varhowto.com/install-miniconda-ubuntu-20-04/

reference

https://www.youtube.com/watch?v=23aQdrS58e0&t=767s


