# UnobservableQueue.jl

| **`Linux`** | **`Windows`** | **`Coverage`** |
|-----------------|---------------------|---------------------|
| [![Build Status](https://travis-ci.org/ajkeith/UnobservableQueue.jl.svg?branch=master)](https://travis-ci.org/JuliaPOMDP/UnobservableQueue.jl) | [![Build status](https://ci.appveyor.com/api/projects/status/6t1b3xel2ilwfo3r?svg=true)](https://ci.appveyor.com/project/ajkeith/unobservablequeue-jl) | [![Coverage Status](https://coveralls.io/repos/github/ajkeith/UnobservableQueue.jl/badge.svg?branch=master)](https://coveralls.io/github/ajkeith/UnobservableQueue.jl?branch=master) |

Order-based estimation algorithm for unobservable queues

## Installation
`Pkg.clone("https://github.com/ajkeith/UnobservableQueue.jl")`

## Algorithm
The order-based estimation algorithm is implemented in src/estimators.jl. This file also includes our implementation of the variance estimator due to Park, Kim & Willemain (2011). The LCFS versions are in src/lcfs.jl.

## Testing
Tests for the correctness of each algorithm are available in test/runtests.jl.

## Micro-Benchmarks
Micro-benchmarks are available in the benchmarks directory.

## Analysis
The experimental design, regression analysis, and plots are located in the analysis directory. All analysis was conducted in JMP.

## Output Data

### FCFS
- *err11.csv*: first replicate of estimation error with column order of order-based, variance, uninformed
- *err12.csv*: second replicate of estimation error with column order of order-based, variance, uninformed
- *err_meas11.csv*: first replicate of estimation error under measurement error with column order of order-based, variance, uninformed
- *err_meas12.csv*: second replicate of estimation error under measurement error with column order of order-based, variance, uninformed
- *conv11.csv*: first replicate of convergence with column order of order-based, variance, uninformed
- *conv12.csv*: second replicate of convergence with column order of order-based, variance, uninformed
- *conv_meas11.csv*: first replicate of convergence with measurement error and with column order of order-based, variance, uninformed
- *conv_meas12.csv*: second replicate of convergence with measurement error and with column order of order-based, variance, uninformed

### LCFS
- *err13.csv*: first replicate of LCFS estimation error with column order of order-based, variance, uninformed
- *err_meas13.csv*: first replicate of LCFS estimation error under measurement error with column order of order-based, variance, uninformed
- *conv13.csv*: first replicate of LCFS convergence with column order of order-based, variance, uninformed
- *conv_meas13.csv*: first replicate of LCFS convergence with measurement error and with column order of order-based, variance, uninformed

### Archived Data
These data files use older versions of the code.
- *err.csv*: first replicate of estimation error with column order of order-based, variance, uninformed
- *err2.csv*: second replicate of estimation error with column order of order-based, variance, uninformed
- *err_meas.csv*: first replicate of estimation error under measurement error with column order of order-based, variance, uninformed
- *err_meas2.csv*: second replicate of estimation error under measurement error with column order of order-based, variance, uninformed
- *conv.csv*: convergence with 400 obs requirement, with column order of order-based, variance, uninformed
- *conv_meas.csv*: convergence with 400 obs requirement and measurement error, with column order of order-based, variance, uninformed
- *conv2.csv*: convergence with 200 obs requirement, with column order of order-based, variance, uninformed
- *conv_meas2.csv*: convergence with 200 obs requirement and measurement error, with column order of order-based, variance, uninformed

## Primary References
Park, J., Kim, Y. B., & Willemain, T. R. (2011). Analysis of an unobservable queue using arrival and departure times. Computers and Industrial Engineering, 61(3), 842–847. https://doi.org/10.1016/j.cie.2011.05.017

## Citing UnobservableQueue.jl
If this code is useful to you, please cite [this paper](https://www.sciencedirect.com/science/article/abs/pii/S0360835219300099#ec-research-data):

```
@article{keith2019order,
title = "An order-based method for robust queue inference with stochastic arrival and departure times",
author = "Andrew Keith and Darryl Ahner and Raymond Hill",
journal = "Computers & Industrial Engineering",
volume = "128",
pages = "711 - 726",
year = "2019",
issn = "0360-8352",
doi = "https://doi.org/10.1016/j.cie.2019.01.005",
url = "http://www.sciencedirect.com/science/article/pii/S0360835219300099",
keywords = "Queueing, Queue inference, Robust, Unobservable"
}
```
