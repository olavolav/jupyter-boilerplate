# Jupyter boilerplate

## Installation

We'll be working in a [Jupyter notebook](https://jupyter.org/) and will use [Virtualenv](https://virtualenv.pypa.io/en/latest/) for installing the dependencies.

### Dependencies

We're assuming that Python 3 and virtualenv are already installed on the system.
Then, after cloning the repository we need to initialize the virtualenv directory and install the dependencies:
```
$ virtualenv venv/
$ pip3 install -r requirements.txt
```

The last part is initializing the kernel that we'll later use in the Jupyter notebook.
```
ipython kernel install --user --name=A_USEFUL_NAME_LIKE_THE_REPO_NAME
```

### Jupyter extensions

The Jupyter extensions and their configuration has already been installed by the preceding steps, but we still need to enable them.

First, we need to enable [nbextensions](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/install.html) itself:
```
jupyter contrib nbextension install --user
```

And then, unless we want to configure the extensions from the command line, we need to enable the [extensions configurator](https://github.com/Jupyter-contrib/jupyter_nbextensions_configurator):
```
jupyter nbextensions_configurator enable --user
```

For the record, I have enabled:

* Collapsible headings
* Autopep8
* Table of Contents (2)



## Launch notebook

Then we can work in the notebook as usual. Just pay attention to select the kernel that we just installed.
```
jupyter notebook
```

The notebook assumes that the CSV data is in the `data/` directory.
