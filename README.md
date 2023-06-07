# Data Thinking Codespace: Running Copilot in Jupyter Notebooks in GitHub Codespaces and Locally

Welcome to your shiny new codespace, data thinkers! We've got everything fired up and running for you to explore Python and Jupyter notebooks and all kinds of artificial intelligence technology such as Copilot and ChatGPT :)

If you use GitHub Codespaces, check out how to version control your code here: https://docs.github.com/en/codespaces/developing-in-codespaces/using-source-control-in-your-codespace

## Environment

Anaconda can be installed using Homebrew on macOS:

```
brew install --cask anaconda
```

Or using Chocolatey on Windows:

```
choco install anaconda3
```

The environment is created using:

```
conda create --name datathinking.org python==3.11 ipykernel altair pandas scikit-learn matplotlib jupyter pip scipy
pip install --upgrade pip
pip install --upgrade "jax[cpu]"
pip install jupysql
pip install duckdb==0.8.0
pip install duckdb-engine
```

You can then activate the environment using:

```
conda activate datathinking.org
```

Select conda as the python interpreter within Visual Studio Code in the codespace to execute the code.

And you can select the environment as the kernel in Jupyter Notebooks using Visual Studio code: https://code.visualstudio.com/docs/datascience/jupyter-kernel-management

