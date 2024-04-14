# Getting Started

## Python Venv

First, install virtualvenv using `pip install virtualenv`.

Now, you can create a venv to work in using `virtualenv --python 3.12.1 venv`

> Note: You need the specified version on python installed on your local computer to run the command above

### Working in the venv

In order to activate the venv to start working in it, use this command:

```bash
# Linux and Mac
source venv/bin/activate

# Windows
.\venv\Scripts\activate
```

To stop working in the venv, use the command: `deactivate`.

### Setting the Jupyter Notebook's Kernel

To set the Jupyter Notebook's Kernel, click the following icon and select the venv you just made.

<img src="static/noterbook-kernel-picker.gif" width="600" />

### Installing Project Dependencies

Use the following command while in the venv to install the project's dependencies:

```bash
pip install -r requirements.txt
```

## Code Formatting and Linting

I like using Ruff to format and lint my python code. This package is installed whenever you [install the project's dependencies](#installing-project-dependencies) and can be used with the following command:

```bash
ruff format .
```

If you want the file to format on save, you can install the VsCode Ruff extension and add these lines to VsCodes' `setting.json` file:

```json
{
  "notebook.formatOnSave.enabled": true,
  "notebook.codeActionsOnSave": {
    "notebook.source.organizeImports": "explicit"
  },
  "[python]": {
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
      "source.organizeImports": "explicit"
    },
    "editor.defaultFormatter": "charliermarsh.ruff"
  }
}
```

# Exporting the Jupyter Notebook

## To PDF

If you want to export the jupyter notebook to pdf, install the packages from [this guide](https://nbconvert.readthedocs.io/en/latest/install.html#installation) and select the option from this dropdown menu:

![alt text](static/image.png)

## To `.tex`

You can use the following command to convert the jupyter notebook to a `.tex` file:

```bash
jupyter-nbconvert --to latex analysis.ipynb
```
