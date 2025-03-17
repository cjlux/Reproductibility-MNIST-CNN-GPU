# Content

This directory contains the notebook `MNIST_CNN_tanh-GPU`, `MNIST_CNN_tanh-GPU-HyperParams.ipynb` and some tools dedicated to the questions 
of the reproducibility of neural networks training  and Hyper-Parameters (Deep Learning content)

This notebooks have been run on an Ubuntu PC tower with a CPU _Intel(R) Xeon(R) W-1390P @ 3.50GHz_ and a NVIDIA Quadro RTX8000 graphic card : for this study the GPU is used.

We use a well know and quite simple example: the classificatio of the MNIST images (handwritten digits).
For the purpose of demo, we illustrate the non-reproducibility with a simple CNN derived from `LeNet5` from Yann LeCun, 
to show the inherent non-reproducibilty of the training and how to fix it. 

## How to use

If you want to run the notebook on your own machine, follow the lines bellow:

1- Install `uv` (project mamager aware of Python Virtual Environment) using the [Astral web page](https://docs.astral.sh/uv/getting-started/installation/#__tabbed_1_2) for your Operating system.

2- Downlod the repository zip, unzip it and go into the directory `Reproductibility-MNIST-DNN-CPU`

3- With the Command Line Interpreter (CLI) of your macine (a `terminal` for Lunx & MacOS or a `window shell` for Windows) type the command :
    
    uv sync

-> this will download and install all the required Python modules in the sub-directory `.venv`

4- Run the jupyter notebook with:
    
    uv run jupyter lab

Remember that the module `tensorflow[add Cuda]` used in this study to use the GPU of the PC.
