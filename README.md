ecg_anomaly
==============================

This repo explores different ML models for timeseries analysis and anomaly detection in ECG data.
The MIT-BIH Dataset contains:

Total 48 half-hour long 2-channel recordings obtained from 47 patients (25 men and 22 women) between the ages of 23 and 89.
Each recording is annotated with the timing and type of arrhythmia (or normal beat) for each heartbeat.
A cardiologist has labeled the beats to identify various types of arrhythmias, such as:
-----------
        Normal beats (N)
        Premature ventricular contractions (PVC)
        Atrial fibrillation (AF)
        Left or right bundle branch block (LBBB/RBBB)

Sampling Rate:

    The ECG signals were sampled at 360 samples per second per channel.
    The signals are high-resolution (11-bit), making them ideal for precision analysis.
    ('MLII' and 'V5' are channel  names).
    

Channels:

    Most recordings include two ECG lead signals recorded simultaneously.

Application:

    The dataset is widely used to develop and evaluate algorithms for arrhythmia detection, heart rate variability analysis, and other cardiac event classification tasks.
    It's useful for both supervised learning (using annotated data) and unsupervised anomaly detection (detecting irregular beats ).
    

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
