# hep-analysis
hep-analysis aims to reproduce the traditional data-analysis workflow in high-energy physics using Python. This allows us to employ the wide range of modern, flexible packages for machine learning and statistical analysis written in Python to increase the sensitivity of our analysis.

![Mbc distribution](examples/plots/readme_plots/mbc.png?raw=true "Sample feature distribution")
![NN output](examples/plots/readme_plots/nn_prob.png?raw=true "Neural Network Output")

## Functionality
### Machine Learning
- [x] Deep Neural Networks - `TensorFlow`
- [x] Gradient Boosted Trees - `XGBoost`, `scikit-learn`, `LightGBM`
- [x] Hyperparameter Optimization - `scikit-learn`
- [ ] Distributed Training

### Statistical Analysis
- [ ] Signal Yield Extraction
  - [ ] Maximum Likelihood
  - [ ] Bayesian Approach
- [ ] Precision Branching Fraction / CP Asymmetry Measurements

## Notebooks
To view the notebooks available in this repo, visit http://nbviewer.jupyter.org/github/Justin-Tan/hep-analysis/tree/master/ and navigate to the relevant sections. 

## Installation
#### hep-analysis
Installation instructions are shown for Ubuntu distributions running Python 3.6. `hep-analysis` should be compatible with most Linux distributions/OSX. <Coming soon>

#### Dependencies
The easiest way to install the majority of the required packages is through [Anaconda](https://www.continuum.io/downloads). Download (if working remotely use `wget`) and run the installer. We recommend creating a separate environment before installing the necessary dependencies.
```
$ conda create -n hep-ml python=3.6 anaconda
```
#### ROOT
Install the binaries from [here](https://root.cern.ch/downloading-root).

#### root_numpy
[Installation instructions](http://scikit-hep.org/root_numpy/install.html). To install in your home directory:
```
$ pip install --user root_numpy
```

#### TensorFlow
[Installation instructions](https://www.tensorflow.org/install/install_sources). We recommend building from source for better performance. If GPU acceleration is required, install the [CUDA toolkit](https://developer.nvidia.com/cuda-toolkit) and [cuDNN](https://developer.nvidia.com/cudnn).

#### XGBoost 
Clone the repo as detailed [here](http://xgboost.readthedocs.io/en/latest/build.html)

#### LightGBM
Clone the [repo](https://github.com/Microsoft/LightGBM/wiki/Installation-Guide). MPI support optional.
```
git clone --recursive https://github.com/Microsoft/LightGBM ; cd LightGBM
mkdir build ; cd build
cmake .. 
make -j
```

## Relevant Projects
* [TensorFlow](https://www.tensorflow.org/). Open-source library for efficient development of neural networks.
* [XGBoost](http://xgboost.readthedocs.io/en/latest/). Distributed gradient boosting classifier implementation.
* [root_numpy](https://github.com/scikit-hep/root_numpy). Bridge between ROOT and Python.
* [Hyperband](https://people.eecs.berkeley.edu/~kjamieson/hyperband.html?utm_content=buffera95c2&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer).
Bandit-based approach to hyperparameter optimization.
