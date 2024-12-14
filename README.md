# Data Project Template

## Adjusting .gitignore

Ensure you adjust the `.gitignore` file according to your project needs. For example, since this is a template, the `/data/` folder is commented out and data will not be exlucded from source control:

```plaintext
# exclude data from source control by default
# /data/
```

Typically, you want to exclude this folder if it contains either sensitive data that you do not want to add to version control or large files.

## Renaming the .env File
To set up your environment variables, you need to rename the `.env.example` file to `.env`. 


# Setting up your environment

Here's how you can set up your local development environment to contribute.

## For R

Uncomment the first line in `.Rprofile` file to enable loading from `renv`


## Use UV (recommended)

1. Make sure you have Python3.12 installed, create a virtual environment,
   and activate it. If you're new to this, here's one way that we recommend:
   1. Install uv: https://github.com/astral-sh/uv?tab=readme-ov-file#getting-started
      or make sure it is up-to-date with:
      ```
      uv self update
      ```
   2. Create a virtual environment:
      ```
      uv venv -p 3.12 --seed
      ```
   3. Activate it. On Linux, this is `. .venv/bin/activate`, on Windows `.\.venv\Scripts\activate`.

2. Install test requirements: `uv pip install -r requirements-dev.txt`
3. Install docs requirements: `uv pip install -r docs/requirements-docs.txt`

You should also install pre-commit:
```
uv pip install pre-commit
pre-commit install
```
This will automatically format and lint your code before each commit, and it will block the commit if any issues are found.


## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── README.md          <- The top-level README for developers using this project
├── data
│   ├── external       <- Data from third party sources
│   ├── interim        <- Intermediate data that has been transformed
│   ├── processed      <- The final, canonical data sets for modeling
│   └── raw            <- The original, immutable data dump
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
└── src                         <- Source code for this project
    │
    ├── __init__.py             <- Makes src a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    │    
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    ├── plots.py                <- Code to create visualizations 
    │
    └── services                <- Service classes to connect with external platforms, tools, or APIs
        └── __init__.py 
```

--------