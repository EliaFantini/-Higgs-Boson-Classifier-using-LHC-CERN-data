<p align="center">
  <img alt="⚛️Higgs_Boson_Classifier" src="https://user-images.githubusercontent.com/62103572/183050158-52a3122b-35c2-4357-929a-f568c7a0ec38.png">
  <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/y/EliaFantini/-Higgs-Boson-Classifier-using-LHC-CERN-data">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/EliaFantini/-Higgs-Boson-Classifier-using-LHC-CERN-data">
  <img alt="GitHub code size" src="https://img.shields.io/github/languages/code-size/EliaFantini/-Higgs-Boson-Classifier-using-LHC-CERN-data">
  <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/EliaFantini/-Higgs-Boson-Classifier-using-LHC-CERN-data">
  <img alt="GitHub follow" src="https://img.shields.io/github/followers/EliaFantini?label=Follow">
  <img alt="GitHub fork" src="https://img.shields.io/github/forks/EliaFantini/-Higgs-Boson-Classifier-using-LHC-CERN-data?label=Fork">
  <img alt="GitHub watchers" src="https://img.shields.io/github/watchers/EliaFantini/-Higgs-Boson-Classifier-using-LHC-CERN-data?abel=Watch">
  <img alt="GitHub star" src="https://img.shields.io/github/stars/EliaFantini/-Higgs-Boson-Classifier-using-LHC-CERN-data?style=social">
</p>


This project aims at classifying the decay signature of events measured by the Large Hadron Collider at CERN, predicting whether it's the one of a Higgs Boson or not, thanks to Logistic Regression.

The problem was part of a Machine Learning [challenge from AICrowd](https://www.aicrowd.com/challenges/epfl-machine-learning-higgs). Our team, called pasta-balalaika, reached the position 50/307 on the leaderboard, with an F1 score of *0.910* and an accuracy	of *0.952*. This project was also done as an assignment of the EPFL course [CS-433 Machine Learning](https://edu.epfl.ch/coursebook/en/machine-learning-CS-433).

## Higgs Boson
The Higgs boson is an elementary particle in the Standard Model of physics which explains why other particles
have mass. Its discovery at the Large Hadron Collider at CERN was announced in March 2013. 

In this project, we applied machine learning techniques to actual CERN particle accelerator data to recreate the process of
“discovering” the Higgs particle. Physicists at CERN smash protons into one another at
high speeds to generate even smaller particles as by-products of the collisions. Rarely, these collisions can produce
a Higgs boson. Since the Higgs boson decays rapidly into other particles, scientists don’t observe it directly,
but rather measure its “decay signature”, or the products that result from its decay process. 

Since many decay signatures look similar, we estimated the likelihood that a given event’s signature was the result of a
Higgs boson (signal) or some other process/particle (background). To do this, we implemented a pre-processing pipeline and different binary classification
techniques and compared their performance with hyperparameters tuning and cross validation.

<img width="600" alt="Hbb_v2" src="https://user-images.githubusercontent.com/62103572/183052578-ba8910b8-ba31-46d8-b5b0-96048ff90941.png">

## Requirements

The easiest way to run the code is to install
Anaconda distribution (available for Windows, macOS and
Linux). To do so, follow the guidelines from the official
website (select python of version 3): https://www.anaconda.com/download/

Additional potential package versions are specified in the requirements.txt

## File description

- experiments/experiments_models.ipynb 

This Jupyter notebook contains our cross validation and hyperparameter experiments with different models

- experiments/experiments_preprocesing.ipynb

This Jupyter notebook contains our experiments with different preprocessing techniques

- experiments/generate_graphs.ipynb

Notebook that generates the graphs for the paper

- helper.py

Contains helper functions which were used for setting up our experiments  

- implementations.py

Contains 6 default required funcitons + additional minimization algorithms, and accoring loss funcitons 

- metrics.py

Contains our implementations of different metrics

- preprocessing.py

Contains methods for the preprocessing of data 

- run.py

Contains the code for reproducing our best submission file

- utils.py

Miscellaneous other functions, e.g. loading data, splitting it, etc..

- requirements.txt

File which includes package requirements for running the code

## Reproducing results

To reproduce our final submission results, simply run `python run.py` with according conda environment activated
