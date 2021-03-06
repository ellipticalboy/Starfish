# Starfish

[![Build Status](https://travis-ci.org/iancze/Starfish.svg)](https://travis-ci.org/iancze/Starfish)

*Starfish* is a set of tools used for spectroscopic inference. We designed the package to robustly determine stellar parameters using high resolution spectral models, however there are many potential applications to other types of spectra, such as unresolved stellar clusters or supernovae spectra.

Website: http://iancze.github.io/Starfish/

Documentation: http://iancze.github.io/Starfish/current/index.html

Copyright Ian Czekala 2013, 2014

`iczekala@cfa.harvard.edu`

If you wish to use this code in your own research, please email me and I can help you get started. Please bear in mind that this package is under heavy development and features may evolve rapidly. If something doesn't work, please fill an [issue](https://github.com/iancze/Starfish/issues) on this repository. If you would like to contribute to this project (either with bugfixes, documentation, or new features) please feel free to fork the repository and submit a pull request!

**Citation**: if you use this code or derivatives in your research, please cite our [paper: Czekala et al. 2015](http://arxiv.org/abs/1412.5177)

# Installation Instructions

## Prerequisites

*Starfish* has several dependencies, however most of them should be satisfied by an up-to-date scientific python installation. We highly recommend using the [Anaconda Scientific Python Distribution](https://store.continuum.io/cshop/anaconda/) and updating to python 3.3 or greater. This code makes no attempt to work on the python 2.x series, and I doubt it will if you try. This package has only been tested on Linux, although it should work well on Mac OSX and Windows provided you can install the dependencies.

Starfish requires the following Python packages:

* numpy
* scipy
* matplotlib
* h5py
* astropy
* cython
* pyyaml
* emcee (custom version required [here](https://github.com/iancze/emcee))

Unless you actively maintain your own scientific python distribution, I recommend installing the Anaconda distribution with python 3.3 or greater , obtainable [here](https://store.continuum.io/cshop/anaconda/). All of these required packages can be installed via Anaconda by doing `conda install pkg` where `pkg` is the name of the package you want to install.

To make sure you are running the correct version of python, start a python interpreter via the system shell and you should see something similar

    $ python
    Python 3.4.1 (default, May 19 2014, 17:23:49)
    [GCC 4.9.0 20140507 (prerelease)] on linux  
    Type "help", "copyright", "credits" or "license" for more information.

If your shell says Python 2.x, try using the `python3` command instead of `python`.

## Installation

For now, we recommended building *Starfish* from source on your machine. Once the features stabilize, there will be an option to install via `pip`.

First, if you have not already done so, create a github [user account](https://github.com/) and [install git](http://git-scm.com/downloads) on your computer.

In order to download a local copy of this repository, ``cd`` to the location where you want it to live and then do

    git clone git@github.com:iancze/Starfish.git
    cd Starfish

To build the cython extensions

    $ python setup.py build_ext --inplace

Since you may want to edit files during active development, it is best to install in `develop` mode

    $ sudo python setup.py develop

You should now be done. Once the package has stabilized, the `develop` command may change to

    $ sudo python setup.py install

To test that you've properly installed *Starfish*, try doing the following inside of a Python interpreter session

    >>> import Starfish

If you see a blank line, then the package successfully installed. If you see any errors, then something went wrong--please file an [issue](https://github.com/iancze/Starfish/issues).

Now that you've successfully installed the code, please see the [documentation](http://arxiv.org/abs/1412.5177) on how to begin using *Starfish* to solve your spectroscopic inference problem.


## Features in development**

* faster GP kernel optimization
* extinction laws
* accretion continuum from veiling
* Moon contamination of spectra

If you wish to help with any of these, please fork the repository and submit a pull request!
