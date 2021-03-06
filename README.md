# BioHackathon2020
## Copenhagen Bioinformatics Hackathon 2020

### The Team
We are a group of master students hailing from the University of Bologna, with backgrounds in Biology, Biotechnologies and Chemistry.
The members:
* Davide Buzzao - MSc Student at the University of Bologna
* Nicola De Bernardini - MSc Student at the University of Bologna
* Maria Silvia Morlino - MSc Student at the University of Bologna
* Vincenzo Palmacci - MSc Student at the University of Bologna

## Overview
In our project we performed explorative analyses on the dataset provided in the challenge, in order to look for trends and correlations. We generated all sorts of rough and quick plots, along with performing dimensionality reduction and clustering analyses.

## Prerequisites
Python 3.7, R 3.6

## Installation
1. Install direnv:
    * run `brew install direnv (macOS)`
    * run `sudo apt-get install direnv (linux)`
2. Install venv (inspired by https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/):
    * run `sudo apt-get install python3-venv`
3. Setup of .bash_profile and .config/direnv (inspired by https://github.com/direnv/direnv/wiki/Python):
    * run `cat direnv_allow.txt >> ~/.bashrc; echo "export PATH=$PATH:local/bin" > "./.envrc"`
    * run `cat venv_allow.txt >> ~/.bashrc; echo "layout python-venv python3.7"  >> "./.envrc"`
    * run `cat direnvrc_config.txt > ~/.config/direnv/direnvrc`
    * run `source ~/.bashrc; direnv allow ./`
4. Install python packages:
    * run `pip install -r requirements.txt`
    * run on R env `BiocManager:install(c("readr","DESeq2","dplyr","ggplot2", "apeglm"))`

## Key files

Pandas Dataframes of encoded data for ML:
* data/liver/liver_with_genes.pkl
* data/pancreas/pancreas_with_genes.pkl

## Project Structure 
```bash
__data/
|   |-- liver/
|   |   |-- generals
|   |   |-- count_matrix/
|   |   |-- tpm_matrix/
|   |   |-- DESeq/
|   |   |__ plot/
|   |-- pancreas/
|   |   |-- generals
|   |   |-- count_matrix/
|   |   |-- tpm_matrix/
|   |   |-- DESeq/
|   |   |__ plot/
|   |__ generals
|
|__local/
    |-- config/
    |   |__ setup_venv
    |-- src
    |   |__ R/python3/bash_scripts
    |-- bin/
    |   |__ symb_links_to_src
    |__ notebooks
        |-- Data_overview.ipynb
        |-- DESeq_data_prep.ipynb
        |__ Toy_ML_setup_RNA_data.ipynb
```