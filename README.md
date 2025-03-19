# Content

This directory contains notebooks  and Python tools dedicated to study:
- `MNIST_CNN_GPU-Reprod.ipynb`: the non-reproducibility of neural networks training and how to fix it
- `MNIST_CNN_GPU-HyperP.ipynb`: the influence of Hyperparameters on the training.

We use a well know and quite simple classification task: the classification of the MNIST images (handwritten digits). For the purpose of demo, we use a simple CNN derived from  Yann LeCun's `LeNet5` 
to show the inherent non-reproducibilty of the training and how to fix it. 

The 2 demo notebooks given in this repository have already been run on a PC/Ubuntu with an _Intel(R) Xeon(R) W-1390P @ 3.50GHz_ CPU and a _NVIDIA Quadro RTX8000_ graphic card : for this study the GPU is used.

## How to use

If you want to run the notebooks on your own machine with NVIDIA GPU, follow the lines bellow:

1- Install `uv` (project mamager aware of Python Virtual Environment) using this [Astral web page](https://docs.astral.sh/uv/getting-started/installation/#__tabbed_1_2) for your Operating system.

2- Downlod the [repository zip](https://github.com/cjlux/Reproductibility-MNIST-CNN-GPU/archive/refs/heads/master.zip) , unzip it and go into the directory `Reproductibility-MNIST-CNN-GPU-master`

3- With the _Command Line Interpreter_ (CLI) of your machine (a `terminal` for Linux & MacOS or a `window shell` for Windows) type the command :
    
    uv sync

-> this downloads and installs all the required Python modules in the sub-directory `.venv`

4- Copy & rename the notebook you want to run by yourself to keep track of the results of the original ones.<br>
If by chance you overwrites the original version of a notebook, you can find a passive copie with the html extension.

5- Run jupyter:
    
    uv run jupyter lab

Nota:  the module `tensorflow[and-cuda]` is installed within this project to ensure that tensorflow is use on the NVIDIA card of the PC, if possible.
