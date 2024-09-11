ecg_anomaly
==============================

This repo explores different ML models for timeseries analysis and anomaly detection in ECG data downloaded from Kaggle  (https://www.kaggle.com/datasets/shayanfazeli/heartbeat)

----------

######  The dataset is already a curated one, and already artificially cleaned. So we don't need a lot of domain knowledge at this point. 

###### The main purpose of this effort is to set the data science artchitecture in place, focus on the ML Flow and training different Models, without extensive focus on data engineering part at this stage.  We will explore a few more datasets later on, which may require data engineering. 

There are two separate datasets: 
	One from Physionet's arrhythmia dataset MIT-BIH, containing 5-classes (Normal heartbeats and others - Classes: ['N': 0, 'S': 1, 'V': 2, 'F': 3, 'Q': 4])
	Second from PTB dataset, where there are 2 classes: Normal vs Abnormal heartbeat.
	
Individual heartbeat examples are sampled at 125 Hz, and padded to make them the same length (188 samples per segment). 

The data is also nicely divided into train and test for MIT-BIH and abnormal vs normal heartbeats for PTB dataset.

The last column of each sample contains label. 

Idea for transfer learning would be to train a model on one dataset, take the trained model and use it for minimal training on another dataset.



-----------

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
