# README for Machine Learning Model Validation Project

This repository contains the code and documentation for validating the "eos74bo" model from the Ersilia Model Hub, focusing on Task 1 of the internship project, which involves checking model bias.

## Project Overview

The goal of this project is to validate the accuracy and reproducibility of the "eos74bo" model, which predicts ADME properties of small molecules. Task 1 specifically involves checking for model bias by running predictions for a list of 1000 diverse molecules and plotting the results in a scatter plot.

## Repository Structure

- **`README.md`**: This file, providing an overview of the project and instructions for reproducing the work.
- **`src/`**: Directory containing source code.
- **`data/`**: Directory containing datasets used for validation.
- **`results/`**: Directory containing output plots and any other result files.
- **`LICENSE`**: License file for the repository.
- **`.gitignore`**: File specifying intentionally untracked files to ignore.

## Getting Started

To reproduce the validation process, follow these steps:

1. **Clone the Repository**: Clone this repository to your local machine using Git.

```bash
git clone <repository_url.git>


## Project Task 3:

Select the paper and get the dataset that used in that paper and make prediction on that.

## The Paper is followed:

<https://slas-discovery.org/action/showPdf?pii=S2472-5552%2822%2906765-X> that used the PAMPA dataset 

## Download the dataset:

the code to download the dataset is below

```from tdc.single_pred import ADME
data = ADME(name = 'PAMPA_NCATS')
split = data.get_split()```


### Data preprocessing

### Run the Predictions