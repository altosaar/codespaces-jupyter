# Data Thinkers ♥️ Jupyter Notebooks in ♥️ GitHub Codespaces ♥️

Welcome to your shiny new codespace, data thinkers! We've got everything fired up and running for you to explore Python and Jupyter notebooks and all kinds of artificial intelligence technology such as Copilot and ChatGPT :)

You've got a blank canvas to work on from a git perspective as well. There's a single initial commit with what you're seeing right now - where you go from here is up to you!

Everything you do here is contained within this one codespace. There is no repository on GitHub yet. If and when you’re ready you can click "Publish Branch" and we’ll create your repository and push up your project. If you were just exploring then and have no further need for this code then you can simply delete your codespace and it's gone forever.

## Environment

Anaconda can be installed using Homebrew on macOS:

```
brew install --cask anaconda
```

Or using Chocolatey on Windows:

```
choco install anaconda3
```

The Anaconda environment is in `environment.yml` in the root of the repository. 

Select conda as the python interpreter within Visual Studio Code in the codespace to execute the code.

Then run the following command to create the environment:

```
conda env create -f environment.yml
```

You can then activate the environment using:

```
conda activate datathinking.org
```

And you can select the environment as the kernel in Jupyter Notebooks using Visual Studio code: https://code.visualstudio.com/docs/datascience/jupyter-kernel-management

The environment is created using:

```
conda create --name datathinking.org \
  python==3.11 \
  ipykernel \
  python-duckdb \
  jupysql=0.6.6 \
  jaxlib \
  jax \
  altair \
  seaborn \
  pandas \
  polars \
  scikit-learn \
  matplotlib \
  pyarrow \
  duckdb-engine \
  dbt-core \
  jupyter \
  notebook \
  pip \
  pyyaml \
  networkx 
```

## Data Processing
Data such as the 311 Calls dataset lives in our Amazon Simple Storage Service (S3) bucket, `s3://datathinking.org`.

Data is cleaned using the data build tool (`dbt`), whose configuration lives in `data_build_tool_for_processing_data/dbt_project.yml` (generated using `dbt init`). 

In the file called `data_build_tool_for_processing_data/new_york_city_311_calls.sql`, you can see the structured query language (SQL) query that is used to clean the data, and in `data_build_tool_for_processing_data/profiles.yml` you can see the credentials for the S3 bucket or the path that the `dbt build` command writes to in executing the SQL query.
