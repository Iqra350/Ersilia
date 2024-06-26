# README for Machine Learning Model Validation Project

This repository contains the code and documentation for validating the **"eos74bo"** model from the Ersilia Model Hub, focusing on Tasks of the internship project, which involves checking model bias.

## Project Overview

The goal of this project is to validate the accuracy and reproducibility of the "eos74bo" model, which predicts ADME properties of small molecules. Task 1 specifically involves checking for model bias by running predictions for a list of 1000 diverse molecules and plotting the results in a scatter plot. and Task 2 reproducibity of results and Task 3 is extrnal data validation from Selected paper
## About Selected model

## Selected model
Kinetic aqueous solubility (μg/mL) was experimentally determined using the same SOP in over 200 NCATS drug discovery projects. A final dataset of 11780 non-redundant molecules and their associated solubility was used to train a SVM classifier. Approximately half of the dataset has poor solubility (< 10 μg/mL), and two-thirds of these low soluble molecules report values of < 1 μg/mL. A subset of the data used is available at PubChem (AID 1645848) <https://pubchem.ncbi.nlm.nih.gov/bioassay/1645848#section=Result-Definitions>.

## Characteristics
- **Input**: Compound
- **Input** Shape: Single
- **Task**: Classification
- **Output**: Probability
- **Output Type**: Float
- **Output Shape**: Single
- **Interpretation**: Probability of a compound having poor solublibity (< 10 µg/ml)

## Repository Structure

- **`README.md`**: This file, providing an overview of the project and instructions for reproducing the work.
- **`src/`**: Directory containing source code.
- **`data/`**: Directory containing datasets used for validation.
- **`results/`**: Directory containing output plots and any other result files.
- **`LICENSE`**: License file for the repository.
- **`.gitignore`**: File specifying intentionally untracked files to ignore.

## Getting Started

### Task 1 - Week 2

### Evaluating the biased
- Have used the project from the mentioned models
- Dowloaded the dataset
- Cleaned the dataset
- Converted the smiles to standard
- Generated the InchyKeys
- Made the predictions
- Ploted the scttered plot

### Task 2 - Week 2

### Reproducibility of Results

Select the paper and get the dataset that used in that paper and make prediction on that.

### The Paper is followed:

<https://slas-discovery.org/action/showPdf?pii=S2472-5552%2822%2906765-X> that used the Solubilty dataset:

### About the Code:
In this notebook, I am loading a list of molecules I obtained from PubChem for solubilty check of drug, and will replicate the results for [Ersilia Hub Model mentioned in link](https://github.com/ersilia-os/eos74bo?tab=readme-ov-file) and for the [git hub code of external sourse mentioned in link](https://github.com/ncats/ncats-adme/tree/master)processing them to make sure I have:

- Some data visulization
- Generate the ROC curve for the original github code
- Generate the ROC curves for the EMH code
  - Outcome generated after standardized smiles
- Make the comparison

**OutCome:**

- Is about the substance id highly Soluble or active class = '0' or Low Soluble or Inactive class = '1'
- Outcome is in the probability

### Github model Run

#### App running in Terminl

![App runing in terminal](https://github.com/Iqra350/Ersilia/raw/main/figures/Screenshot%202024-03-28%20104831.png)

#### Download the Dataset for prediction

![Download the Dataset](https://github.com/Iqra350/Ersilia/raw/main/figures/Screenshot%202024-03-28%20122950.png)

#### Upload the Dataset for predictions

![Upload the Dataset for predictions](https://github.com/Iqra350/Ersilia/raw/main/figures/Screenshot%202024-03-28%20122935.png)

### Task 3 - Week 3

**PAMPA, parallel artificial membrane permeability assay**: PAMPA is a laboratory test used in drug development to assess how easily a drug can pass through cell membranes. It helps researchers understand the ability of a drug to be absorbed into the bloodstream, which is important for determining its effectiveness.

### Download the  External dataset:

the code to download the dataset is below

```
from tdc.single_pred import ADME
data = ADME(name = 'PAMPA_NCATS')
split = data.get_split()

```


