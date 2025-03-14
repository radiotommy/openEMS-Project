# CUDA-Accelerated Fork of openEMS 

This repository is a fork of the original openEMS project with added support for CUDA-based GPU acceleration in Finite-Difference Time-Domain (FDTD) simulations. The primary goal is to leverage NVIDIA GPUs to improve performance for computationally intensive tasks.

Its still a working in prograss. Currently only the core functionality and ULMP boundary conditions are implemented.

## Prerequisites:
to build this fork with CUDA suport, you'll need:
- CUDA Toolkit: Install the NVIDIA CUDA Toolkit by following the [official NVIDIA installation guilde](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/)


## Build Instructions
1. **Clone the Repository**  
   ```bash
   git clone https://github.com/radiotommy/openEMS-Project.git -b with-cuda
   cd openEMS-Project
   git submodule update --init --recursive

3. **Build the Project**  
    ```bash
    cmake -DWITH_CUDA=1 [any other options you like, follow the official instructions] ..

## How to use
    To run the simulation with gpu, you have to add "engine=cuda" to the openEMS arguments. 

## Note
    this is only the shell of multiple subprojects to help build the whole tool set all togather. The real implementation and development happens in the openEMS sub repository.