text_classification_task
==============================

This is the project for text classification.

Project Organization
------------

    |
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries.
    │
    ├── notebooks          <- Jupyter notebooks.
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    |
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module.
    │   │
    │   ├── data           <- Scripts to download or generate data.
    │   │   ├── clean_text.py
    │   │   └── lemmatize_text.py
    │   ├── features       <- Scripts to turn raw data into features for modeling.
    │   |
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions.
    │   │   └── train.py
    │   │
    │   │
    │   └── utils          <- Scripts for stable preprocessing pipelines creation.
    │       ├── constants.py
    │       └── preprocessing.py
    |
    ├── app.py             <- Script with FastAPI app for model inference.
    |
    ├── Dockerfile         <- Dockerfile for creating isolated env for our inference app.
    |
    ├── poetry.lock        <- poetry.lock file for locking the dependencies.
    |
    └── pyproject.toml     <- pyproject.toml file with project info and all the dependencies that are used.


--------

How to run inference up locally:
1. Install Python
2. In CMD: pip install poetry
3. poetry install (it will automatically install all the dependencies from lock file)
4. poetry shell
5. uvicorn app:app  --port 8000 --reload
6. From localhost:8000 move to localhost:8000/docs
7. Try it :)

How to run inference as a container:
1. Install Docker
2. In cmd: docker build -t text_classification_app .
3. docker run -p 8000:80 text_classification_app
4. From localhost:8000 move to localhost:8000/docs
5. Try it :)

## What else could be used/improved:
### Data Science track:
1. Try Deep Learning approach for text classification (RuBERT)
2. Deep dive in text (maybe there are outlier: advertisments for example)
3. If outliers detected (train a model that will detect this outliers and remove them)
4. Better Hyperparameter optimization (Use AWS Batch or create local Kubernetes cluster for this task)
5. Compare model results using statistical approach

### FastAPI track (backend)
1. More routes to control the user inputs, data saving
2. Connect app with Database (store the data, logs, etc.)

### MLOPS
1. CI/CD pipelines setting
2. Use Mlflow for model tracking
3. Use Prometheus for monitoring FastAPI app
4. Use Grafana for visualization
5. Evedently for model drift
6. DVC for data controlling  and for pipelines creation
