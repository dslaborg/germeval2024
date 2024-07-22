# GermEval2024
## Installation
To install the correct versions of the required packages run `$ pip install -r requirements.txt` 
and `$ pip install -r custom-requirements.txt`. This instructions have been tested with a Python 3.8 interpreter
exclusively

## Preprocessing
The Notebook `1_preprocessing.ipynb` reads the dataset of the GermEval2024 and stores the data in a better format for
further processing. Additionally it produces some graphics that give statistical insight into the dataset.

## Grid Search
To carry out a Grid Search that produces models with the best parameter set for each annotator an classifier
on the embeddings of each embedding-model, execute `2_parameter_grid_search.ipynb`. This also produces and stores
the sentence-embeddings of each dataset.

## Model Testing
The Notebooks `3_st1_model_testing.ipynb` and `3_st2_model_testing.ipynb` use the models produced by the grid search
to evaluate their scoring int Subtask 1 and Subtask 2 on the Validation set. 

## Submission
To reproduce the Datasets that have been submitted to GermEval, execute the Notebooks starting with `4_submission_`.
The created output files are written to `created_data/results`.