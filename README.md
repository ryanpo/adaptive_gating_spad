# Data and Python code used in "Adaptive Gating for Single-Photon 3D Imaging"
Methods in this code use photon histograms captured by a gated SPAD operating in fixed gated mode. SPAD acquisition is then simulated by resampling the photon arrival distributions, which can be found in the data folder.

Experimental results from the main paper are reproducible using the code provided in 'adaptive.py'. The code implements adaptive gating and free-running mode under fixed or adaptive exposure times, it is also able to incorporate depth priors into the MAP estimator model. Data is contained in the 'data' folder, but not included in this repo due to size contraints, data for the "Leaf" scene can be downloaded from the following link https://www.dropbox.com/sh/q6s81b6qy8fw8an/AAAULOmZScDbvraB3wy5qpkQa?dl=0. The 'experiments' folder contains two scripts: 'fixed_exposure' which is currently configured to reconstruct the "Leaf" scene with a fixed exposure of 100microseconds using free-running mode and adaptive gating, and 'adaptive_exposure' which is also configured to reconstruct the "Leaf" scene using adaptive exposure with entropy threshold of 0.25. Code can easily be reconfigured to use data collected for other scenes, such as the "Horse" scene, this data is not included due to size constraints. By default, all reconstructions use the MAP estimator.

The given code has been tested on Python 3.6 under Linux, on a 1.7GHz laptop with 16GB of RAM.
