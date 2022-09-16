# Quantum-Sparcle

Python modules for simulating and manipulating VLBI data and producing images with regularized maximum likelihood methods. This version is an early release so please raise an issue, submit a pull request, if you have trouble or need help for your application.

The package contains several primary classes for loading, simulating, and manipulating VLBI data. The main classes are the Image, Movie, Array, Obsdata, Imager, and Caltable classes, which provide tools for loading images and data, producing simulated data from realistic u-v tracks, calibrating, inspecting, and plotting data, and producing images from data sets in various polarizations using various data terms and regularizing functions.

Installation
The latest stable version (1.2.4) is available on PyPi. Simply install pip and run

pip install ehtim
Incremental updates are developed on the dev branch. To use the very latest (unstable) code, checkout the dev branch, change to the main eht-imaging directory, and run:

pip install .
Installing with pip will update most of the required libraries automatically (numpy, scipy, matplotlib, astropy, ephem, future, h5py, and pandas).

If you want to use fast fourier transforms, you will also need to separately install NFFT and its pynfft wrapper. The simplest way is to use conda to install both:

conda install -c conda-forge pynfft
Alternatively, first install NFFT manually following the instructions on the readme, making sure to use the --enable-openmp flag in compilation. Then install pynfft, with pip, following the readme instructions to link the installation to where you installed NFFT. Finally, reinstall ehtim.

Certain eht-imaging functions require other external packages that are not automatically installed. In addition to pynfft, these include networkx (for image comparison functions), requests (for dynamical imaging), and scikit-image (for a few image analysis functions). However, the vast majority of the code will work without these dependencies.
