# Modelling COVID-19 dynamics and potential for herd immunity by vaccination in Austria, Luxembourg and Sweden

## Description: 
This code represents the implementation of our extended SEIR model with ICU, hospital, recovering, death and vaccination. With this code, we generated the results and simulations of the manuscript [1]. 

## Structure of the code (Pseudocode): 
1) Importing dataset
2) Computing seven days moving average
3) Creation of a calender for the plots
4) If needed: part for fitting procedure of the prevelance data in order to find a function p1
5) Just for Sweden: fitting procedure in order to find a p2 function to describe the behavior
6) ODE system based on SEIR
7) Introduction of social interaction function as a step-wise function
8) Solving of ODE system
9) Plotting and simulation of three different social interaction-scenarios (cumulative cases, daily cases, death, ICU and hospital)
10) Likelihood function for the different waves 
11) Parallel MCMC
12) Gelman-Rubin diagnostic
13) 2D density plot
14) Fold change plot
15) Vaccination part with different vaccination strategies
16) Simulation of different vaccination scenarios
17) Heat map for herd immunity by April
18) Heat map for herd immunity over time

## Table of Contents:
This repository contains different types of formats. We have different excel sheets which contain the data until 15th December.
- The excel file: Sweden_data.xlsx contains the data for Sweden until 15th December.
- The excel file : Austria.xlsx contains the data for Austria until 15th December.
- The excel file: Lux-trial_15December.xlsx contains the data for Luxembourg until 15th December.
- The Jupyter notebook: Luxembourg_Residents_Fit_1st_and_2nd_wave_Optimize_and_MCMC_ParallelFullChains.ipynb is the code for Luxembourg.
- The Jupyter notebook: new_model_for_Sweden_minimize-latest-version.ipynb is the code for Sweden.
- The Jupyter notebook: Austria_main_model.ipynb is the code for Austria.

## How to run the scripts

To run our code:
- Download the full content of the directory containing this README file.
- Make sure you have installed Jupyter (we developed the code under version: jupyter-notebook : 6.1.4, so we suggest this or subsequent versions). Additionally, the code has been tested on macOS Sierra 10.12.6 and should run on every OS.
- Open Jupyter.
- Select the script corresponding to the analysis you are interested in running, and run it.


We used the following libraries and version of the libraries :
- sys==Python BuiltIn
- xlrd==1.2.0
- seaborn==0.9.0
- scipy==1.5.2
- pymcmcstat==1.9.0
- pymc3==3.8
- pandas==1.1.1
- numpy==1.19.1
- mcmcplot==1.0.1
- matplotlib==3.3.1
- lmfit==1.0.1

More information of what concretly is used in relation to Jupyter:
- jupyter core   : 4.6.3
- jupyter-notebook : 6.1.4
- qtconsole    : 4.7.6
- ipython     : 5.1.0
- ipykernel    : 5.3.4
- jupyter client  : 6.1.6
- jupyter lab   : 2.2.8
- nbconvert    : 5.4.1
- ipywidgets    : 7.5.1
- nbformat     : 5.0.7
- traitlets    : 4.3.3 


## Credits
To use our original or adapted codes, please cite our work https://doi.org/10.1101/2020.12.31.20249088 as [1], see reference at the end of this document.

The Jupyter notebook code present in this directory has been written by Françoise Kemp and Stefano Magni, with contributions from Daniele Proverbio, Laurent Mombaerts, Atte Aalto,  Aymeric Fouquier d'Hérouël, Andreas Husch, Christophe Ley, Jorge Gonçalves and Alexander Skupin. This work can be found as a preprint in the manuscript **[1]** which can be downloaded from MedrXiv https://doi.org/10.1101/2020.12.31.20249088 (currently submitted for journal publication) and titled "Stages of COVID-19 pandemic and paths to herd immunity by vaccination: dynamical model comparing Austria, Luxembourg and Sweden". 
