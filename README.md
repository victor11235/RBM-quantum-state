# RBM-quantum-state


Updated: 2022-04-12

File Descriptions (*---"not too important"; **---"fairly important"; ***---"very important"):

***.ipynb_checkpoints (and other ipynb notebook files outside folders): Please see the .ipynb files outside the folders, they contain the same code. These notebook files were created for analysis tasks or quick tests. Important ones include, Analysis_energy_over_iteration.ipynb (used for energy descent visualization), Analysis_Time_scaling.ipynb (file for analyzing time-scaling behaviors of ground state), spectrum.ipynb (used to generate spectrum plot, based on Alev's original implementation). 

**2021_summer_data: Contains data from 2021 summer to 2022 winter break, sorry for the confusing name... You can view it as a big container of data, as most analysis notebooks need them. 

***2022_winter_analysis: Contains datasets and analysis notebooks after 2022 winter break. One important analalysis notebook is the excited state histogram using penalty method, as it produces one of the key figures in the report.

*Analysis_eng_er: This is from 2021 summer, where work was done to see how does the final energy error depends on the diagonal shift and N. This was done in a histogram manner, where 50 runs were done and the criteria is to check whether the final energy error is less than half of the energy gap.

*Analysis_excited_states: This is from 2021 summer, where we attempted to calculate excited states using outer product of state vector in dense form, and did some analysis, including a histogram and an investigation on the choice of the lifting factor.

*Analysis_stopping: This is from 2021 summer, where we tried to use a stopping condition and count the number of iterations to quantify the time-scaling of N. Note that the stopping condition used here is that, stop the iterations if two consecutive energy expectation values have a difference less than the threshold (not too useful here, also in the early slides, I think I interpreted the stopping condition incorrectly). 

**Dynamics: This is from 2021 summer, where spin dynamics, correlation function, and linear response were done using dense state vectors, i.e. not efficient for large N. This folder has a separate "2021_summer_data" sub-folder containing data for dynamics folder only. Many of the code for "efficient dynamics" were adopted from here.

Time-scaling with accuracy: Ignore it please, it has nothing, all the time scaling stuff were done in Analysis_Time_scaling.ipynb, the separate notebook file outside folders.

***efficient dynamics: !!! most important folder of files, as it contains all the dynamics done in an efficient Monte Carlo manner. The "eigenstate_data" folder has the output eigenstate data in the form of stored RBM parameters. Here are some important files: 1."correlation function.ipynb" has calculations for correlation function, as well as a FFT spectrum done numerically; 2."correlation_function_analytic_spectrum.ipynb" has correlation function calculations updated with error bars, as well as an analytic spectrum with unit impulse functions to represent Dirac-Delta functions; 3."expectation_value_test" has the code for generating samples of the initial correlation function at t=0, also generating a histogram based on it, as well as an extrapolation of fluctuation standard deviation; 4."linear_response.ipynb" has the calculations and figures for the linear response of Sx and Sy, using correlation function of S+ and S-, both exactand approximate RBM solutions.

*excited states: 


