# Boosted Decision Tree Omnifold

## Overview

Provide a brief overview of what your project does and its purpose. This can include a few sentences describing the functionality of your code and the context in which it is used.

## Prerequisites

Before you begin, ensure you have the following software installed on your system:

- [Git](https://git-scm.com/)
- [Conda](https://docs.conda.io/en/latest/miniconda.html) (Miniconda/Anaconda)
- [CMake](https://cmake.org/) (for building RooUnfold)

## Installation Instructions

Follow these steps to set up the environment and dependencies required for this project.

### 1. Clone Dependency Repositories

First, clone the following repositories into your home directory as they are required dependencies:

```bash
git clone https://github.com/rymilton/unfolding.git ~/unfolding
git clone https://github.com/ericmetodiev/OmniFold.git ~/OmniFold
git clone https://github.com/ViniciusMikuni/OmniLearn.git ~/OmniLearn
git clone https://gitlab.cern.ch/RooUnfold/RooUnfold.git ~/RooUnfold
```

###  2. Build RooUnfold

Once you've cloned the RooUnfold repository, navigate to the directory and build it using the following commands:

```bash
cd ~/RooUnfold
mkdir build
cd build
cmake ..
make -j4
cd ..
source build/setup.sh
```

### 3. Set Up Conda Environment

To ensure all required Python dependencies are installed, create the conda environment using the provided `environment.yml` file.

```bash
conda env create -f environment.yml
conda activate <environment_name>
```