## Stochastic Variance-Reduced Iterative Hard Thresholding in Graph Sparsity Optimization

## Overview

This repository houses the code for "Qianqian Tong, Derek Fox, and Samuel Hernandez, Stochastic Variance-Reduced 
Iterative Hard Thresholding in Graph Sparsity Optimization".

This code is based off of the excellent work found in: "Baojian Zhou, Feng Chen, and Yiming Ying, 
Stochastic Iterative Hard Thresholding for Graph-structured Sparsity
Optimization, ICML, 2019".

Our code is written in Python. The implementation of head and tail 
projection are from the aforementioned paper, written in C11.

## Instructions

Below are the installation instructions:

    0.  Clone the code to your machine: git clone https://github.com/Derek-Fox/graph-scsg-iht.git

    1.  Install python2.7 and gcc. I highly suggest setting up a conda/venv environment to make this easy!!

    2.  Install numpy, scikit-learn, matplotlib, and networkx.

    3.  After the above three steps, run: python setup.py build_ext --inplace.

After step 3, it will generate a sparse_module.so file, which will allow for the head and tail projections from
Zhou et al. to run properly.

## Run Experiments

To run tune_params.py, simply run `python tune_params.py` in your terminal. In the main method,
you can comment out the function calls to determine which parameters to tune/generate figures for.

To run exp_sr_test02, call `python exp_sr_test02.py run_test <num_cpus>` with the number of cpus to use.

To run exp_bc_run, call `python exp_bc_run.py <num_cpus> <trial_idx_start> <trial_idx_end>` with the number
of cpus, and the beginning and end trial numbers to run. For instance, to run 20 trials, you would call
`python exp_bc_run.py <num_cpus> 0 20` with the appropriate number of cpus for your system.
