# RBM-quantum-state


Updated: 2022-04-12

__Package Version:__
Name: netket
Version: 3.3
Summary: Netket : Machine Learning techniques for many-body quantum systems.
Home-page: http://github.com/netket/netket
Author: Giuseppe Carleo et al.
Author-email: netket@netket.org
License: Apache 2.0
Location: /Users/victorwei/opt/miniconda3/lib/python3.8/site-packages
Requires: jaxlib, optax, plum-dispatch, numba4jax, numpy, numba, tqdm, flax, jax, orjson, scipy, igraph

__File Descriptions__ (*---"not too important"; **---"fairly important"; ***---"very important"):

__***.ipynb_checkpoints (and other ipynb notebook files outside folders)__: Please see the .ipynb files outside the folders, they contain the same code. These notebook files were created for analysis tasks or quick tests. Important ones include, Analysis_energy_over_iteration.ipynb (used for energy descent visualization), Analysis_Time_scaling.ipynb (file for analyzing time-scaling behaviors of ground state), spectrum.ipynb (used to generate spectrum plot, based on Alev's original implementation). 

__**2021_summer_data:__ Contains data from 2021 summer to 2022 winter break, sorry for the confusing name... You can view it as a big container of data, as most analysis notebooks need them. 

__***2022_winter_analysis__: Contains datasets and analysis notebooks after 2022 winter break. One important analalysis notebook is the excited state histogram using penalty method, as it produces one of the key figures in the report.

__*Analysis_eng_er:__ This is from 2021 summer, where work was done to see how does the final energy error depends on the diagonal shift and N. This was done in a histogram manner, where 50 runs were done and the criteria is to check whether the final energy error is less than half of the energy gap.

__*Analysis_excited_states:__ This is from 2021 summer, where we attempted to calculate excited states using outer product of state vector in dense form, and did some analysis, including a histogram and an investigation on the choice of the lifting factor.

__*Analysis_stopping:__ This is from 2021 summer, where we tried to use a stopping condition and count the number of iterations to quantify the time-scaling of N. Note that the stopping condition used here is that, stop the iterations if two consecutive energy expectation values have a difference less than the threshold (not too useful here, also in the early slides, I think I interpreted the stopping condition incorrectly). 

__**Dynamics:__ This is from 2021 summer, where spin dynamics, correlation function, and linear response were done using dense state vectors, i.e. not efficient for large N. This folder has a separate "2021_summer_data" sub-folder containing data for dynamics folder only. Many of the code for "efficient dynamics" were adopted from here.

__Time-scaling with accuracy:__ Ignore it please, it has nothing, all the time scaling stuff were done in Analysis_Time_scaling.ipynb, the separate notebook file outside folders.

__***efficient dynamics:__ !!! one of the most important folder of files, as it contains all the dynamics done in an efficient Monte Carlo manner. The "eigenstate_data" folder has the output eigenstate data in the form of stored RBM parameters. Here are some important files: 
1."correlation function.ipynb" has calculations for correlation function, as well as a FFT spectrum done numerically;<br/> 2."correlation_function_analytic_spectrum.ipynb" has correlation function calculations updated with error bars, as well as an analytic spectrum with unit impulse functions to represent Dirac-Delta functions;<br/> 
3."expectation_value_test" has the code for generating samples of the initial correlation function at t=0, also generating a histogram based on it, as well as an extrapolation of fluctuation standard deviation;<br/> 
4."linear_response.ipynb" has the calculations and figures for the linear response of Sx and Sy, using correlation function of S+ and S-, both exactand approximate RBM solutions.

__*excited states:__ This folder contains a failed attempt of making excited state calculation efficient by making local operator module sparse-matrix-compatible.

__***penalty excited state:__ !!! one of the most important folder of files, as it contains the calculations of excited states using penalty-based method, which is efficient. <br/> The two "expect_grad_ex.py" and "vmc_ex.py" files are the modified module files that will be imported in order to run penalty-based excited state calculations. <br/> Folder "2021_summer_data" is the local data folder for storing output files of penalty-excited states. <br/> Folder "Validation Test" contains time-scaling verifrication of the penalty method. <br/> Folder "Exploration Test" contains experiments involving changing penalty coefficient, RBM's hidden nodes number (alpha), optimizer (rmsprop v.s. vanilla SGD), and a local data storage folder.




