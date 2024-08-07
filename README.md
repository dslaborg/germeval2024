# GermEval2024

Repository containing the experiments described in our paper for the GermEval 2024 challenge: *"Detecting Sexism in German Online Newspaper Comments with Open-Source Text Embeddings (Team GDA, GermEval2024 Shared Task 1: GerMS-Detect, Subtasks 1 and 2, Closed Track)"*.

**Authors:** Florian Bremm, Patrick Gustav Blaneck, Tobias Bornheim, Niklas Grieger and Stephan Bialonski

This README provides instructions on how to set up the environment, preprocess the data, perform a grid search for model parameters, test models, and generate submission files.

## Installation

To install the required packages, run the following commands in your terminal:

```sh
pip install -r requirements.txt
pip install -r custom-requirements.txt
```

These instructions have been tested with Python 3.8 exclusively.

## Preprocessing

The notebook `1_preprocessing.ipynb` reads the GermEval2024 dataset and stores the data in a more suitable format for further processing.
Additionally, it generates graphics that provide statistical insights into the dataset.

## Grid Search

To perform a grid search and obtain the best parameter sets for each annotator and classifier on the embeddings of each embedding model, execute `2_parameter_grid_search.ipynb`.
This notebook also generates and stores the sentence embeddings for each dataset.

## Model Testing

The notebooks `3_st1_model_testing.ipynb` and `3_st2_model_testing.ipynb` use the models generated by the grid search to evaluate their performance in Subtask 1 and Subtask 2 on the validation set.

## Submission

To reproduce the datasets submitted to GermEval, execute the notebooks starting with `4_submission_`.
The output files will be written to the `created_data/results` directory.