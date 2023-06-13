# Data Thinking Codespace: Running Copilot in Jupyter Notebooks in GitHub Codespaces and Locally

Welcome to your shiny new codespace, data thinkers! We've got everything fired up and running for you to explore Python and Jupyter notebooks and all kinds of artificial intelligence technology such as Copilot and ChatGPT :)

If you use GitHub Codespaces, check out how to version control your code here: https://docs.github.com/en/codespaces/developing-in-codespaces/using-source-control-in-your-codespace

## How to install the data thinking environment

Anaconda can be installed using Homebrew on macOS:

```
brew install --cask anaconda
```

Or using Chocolatey on Windows:

```
choco install anaconda3
```

Once anaconda is installed, the environment can be created using the following commands in the terminal (https://missing.csail.mit.edu/2020/course-shell/; open the shell in Visual Studio Code using `Ctrl + Shift + P` and typing `Terminal: Create New Terminal`):

```
conda create --name datathinking.org python==3.11 ipykernel altair pandas scikit-learn matplotlib jupyter pip scipy
```

Then, activate the environment using:

```
conda activate datathinking.org
```

And install the following packages:

```
pip install --upgrade pip
pip install --upgrade "jax[cpu]"
pip install jupysql
pip install duckdb==0.8.0
pip install duckdb-engine
pip install fastparquet pyarrow
pip install "vegafusion[embed]"
pip install "vegafusion-jupyter[embed]"
pip install polars
```

Next, clone this repository in Visual Studio Code (instructions here: https://code.visualstudio.com/docs/sourcecontrol/overview).

Then, open one of the Jupyter notebooks with `.ipynb` extension from inside Visual Studio Code that has the `datathinking.org-codespace` repository open.

Then, select the `datathinking.org` environment in the python interpreter within Visual Studio Code in the codespace to execute the code.

And you can select the environment as the kernel in Jupyter Notebooks using Visual Studio code: https://code.visualstudio.com/docs/datascience/jupyter-kernel-management. You may need to reload the window to see the `datathinking.org` kernel (open the command palette and type `Developer: Reload Window`).

## Debugging Notes

* To remove the `datathinking.org` environment, use the following command:

```
conda deactivate && conda env remove -n datathinking.org
```

* To uninstall anaconda on homebrew:

```
brew uninstall anaconda --cask
```

* On Windows machines, we recommend using Windows Subsystem Linux and Visual Studio code. Windows Subsystem Linux can be installed here: https://learn.microsoft.com/en-us/windows/wsl/install

* For issues related to `conda` not being found, it might be because the homebrew software was unable to add the `conda` command to the `PATH`. This can usually be fixed on Mac by opening (or creating, if it doesn't exist) a file in the user directory called `~/.zshrc` for zshell or `~/.bashrc` for bash, and adding the following line: 

```
export PATH=/anaconda3/bin:$PATH
```

* You can check whether the Anaconda path is on your terminal's `PATH` variable by using the `echo` command to print the contents of a command line variable: 

```
echo $PATH
```

If you don't see Anaconda's path listed, you might need to find it using:

```
echo $HOMEBREW_PREFIX
ls $HOMEBREW_PREFIX/anaconda3/bin
```

And seeing if these directories exist or not.

