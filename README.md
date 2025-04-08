
# 1. Setting up your environment

Here's how you can set up your local development environment.

## For R

It is uncommon to setup a virtural environment in an R project. In case you need it, do the following steps:

1. Install rig: https://github.com/r-lib/rig
   
2. Install a specific R version
   ```
   rig add release
   ```
3. Restore project library from a lockfile
   ```r
   renv::restore()
   ```
4. Uncomment the first line in `.Rprofile` file to enable loading from `renv`

## For Python

1. Install uv: https://github.com/astral-sh/uv?tab=readme-ov-file#getting-started or make sure it is up-to-date with:
   ```
   uv self update
   ```

2. Create a virtual environment:
   ```
   uv venv -p 3.12 --seed
   ```

3. Activate it. On Windows, this is `.\.venv\Scripts\activate`.

##  Adjusting .gitignore

Ensure you adjust the `.gitignore` file according to your project needs. For example, the `/data/` folder by default will not be inlucded from source control because it contains either sensitive data that you do not want to add to version control or large files. To include it, simply remove the comment from the line:

   ```plaintext
   # exclude data from source control
   # /data/
   ```

## Renaming the .env File
To set up your environment variables, you need to rename the `.env.example` file to `.env`. 

--------
# 2. Project Organization

```
├── LICENSE                     <- Open-source license if one is chosen
├── README.md                   <- The top-level README for developers using this project
├── data
│   ├── external                <- Data from third party sources
│   ├── interim                 <- Intermediate data that has been transformed
│   ├── processed               <- The final, canonical data sets for modeling
│   └── raw                     <- The original, immutable data dump
│
├── images                      <- Contains all media assests of the project
│
├── references                  <- Zotero library and all relevant pdf documents
│
├── models                      <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks                   <- Jupyter notebooks and Quarto documents, used to generate reports
│
├── references                  <- Data dictionaries, manuals, and all other explanatory materials
│
├── reports                     <- Generated analysis as HTML, PDF, LaTeX, etc.  
│   └── figures                 <- Generated graphics and figures to be used in reporting
│
└── src                         <- Source code for this project
    │
    ├── __init__.py             <- Makes src a Python module
    │    
    ├── modeling                <- Contain code for modelling tasks
    │   ├── __init__.py 
    │
    └── utils                   <- Contains for data wrangling and transformation
        ├── __init__.py 
```

# 3. Render the project

Render with Quarto

```
quarto preview
quarto render
```

Render with MystMD

```
myst start
```


# 4. CHANGELOG

### 2025-04-10
<details>

- Every changes should be documented here

</details>