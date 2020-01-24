Cookiecutter Data Project Repositories Structure Template
==============================
[cookiecutter](https://cookiecutter.readthedocs.io/en/latest/installation.html) is a _'logical, reasonably standardized, but flexible project structure for doing and sharing data science work.'_
It helps with projects reproducibility, code quality and collaboration within data science teams. This fork of the main structure is a barebone structure that can be further customized to answer not only data science
needs but also analytics engineering or even ad-hoc analysis projects as well.

This custom template is released under the MIT license so feel free to use it for all yours projects.

A few choices have been made regarding its content:
* The [pipenv](https://pipenv.readthedocs.io/en/latest/) library for Python dependencies management is used by default.
* To check the quality of our code follows PEP8 standards, we use [flake8](https://pypi.org/project/flake8/).
* We use a [Makefile](https://en.wikipedia.org/wiki/Makefile) to run recurring commands (linter, requirements). More can be added once installed.


### Prerequisites
------------
  - [cookiecutter](https://cookiecutter.readthedocs.io/en/latest/installation.html)
  ```bash
  $ pip install cookiecutter
  ```


### Install the structure in a new empty project folder
------------
```bash
$ cookiecutter https://github.com/GuillaumeLegoy/data-projects-template.git
```


### Once inside your project, run the following to install dev dependencies:
------------
```bash
$ make requirements
```


### To make sure your code follows pep8 standards run the following inside your project:
------------
```bash
$ make lint
```

### If you are developing a Python library, sync your Pipfile Python libraries with setup.py:
------------
```bash
$ make setup
```


### Directory structure
------------
```
├── /src                <- Source code for use in this project.
│   └── __init__.py     <- Makes src a Python module
│
├── /test
│
├── Makefile           <- Makefile with commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
│
├── .flake8            <- Flake8 linter parameters
├── .gitignore         <- Gitignore for Python projects
├── Makefile           <- Makefile including 3 commands: `requirements`, `lint`.
├── Pipfile            
├── Pipfile.lock       <- The requirements files for reproducing the analysis environment
├── README.md
└── setup.py           <- Setup file to package your library or application.
```
