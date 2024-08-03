# Python Commands

## Overview
- [Python Commands](#python-commands)
  - [Overview](#overview)
  - [Installing Python](#installing-python)
  - [Checking Python Version](#checking-python-version)
  - [Running a Python Script](#running-a-python-script)
  - [Installing Packages with pip](#installing-packages-with-pip)
  - [Uninstalling Packages with pip](#uninstalling-packages-with-pip)
  - [Listing Installed Packages](#listing-installed-packages)
  - [Creating a Virtual Environment](#creating-a-virtual-environment)
  - [Activating a Virtual Environment](#activating-a-virtual-environment)
  - [Deactivating a Virtual Environment](#deactivating-a-virtual-environment)
  - [Freezing Package Versions](#freezing-package-versions)
  - [Upgrading pip](#upgrading-pip)
  - [Checking for Package Vulnerabilities](#checking-for-package-vulnerabilities)

## Installing Python

To install Python, download the installer from the [official Python website](https://www.python.org/downloads/) and follow the instructions for your operating system.

## Checking Python Version

To check the version of Python installed:

```sh
python --version
```


To check the version of pip (Python package manager) installed:

```sh
pip --version
```

## Running a Python Script

To run a Python script:

```sh
python script-name.py
```


Replace `script-name.py` with the name of your Python script.

## Installing Packages with pip

To install a package using pip:

```sh
pip install package-name
```

Replace `package-name` with the name of the package you want to install.

## Uninstalling Packages with pip

To uninstall a package using pip:

```sh
pip uninstall package-name
```

Replace `package-name` with the name of the package you want to uninstall.

## Listing Installed Packages

To list all installed packages:

```sh
pip list
```

## Creating a Virtual Environment

To create a virtual environment:

```sh
python -m venv env-name
```

Replace `env-name` with the name of your virtual environment.

## Activating a Virtual Environment

To activate a virtual environment:

For macOS and Linux:

```sh
source env-name/bin/activate
```

For Windows:

```sh
.\env-name\Scripts\activate
```

Replace `env-name` with the name of your virtual environment.

## Deactivating a Virtual Environment

To deactivate the virtual environment:

```sh
deactivate
```

## Freezing Package Versions

To freeze the current package versions into a `requirements.txt` file:

```sh
pip freeze > requirements.txt
```

## Upgrading pip

To upgrade pip to the latest version:

```sh
pip install --upgrade pip
```

## Checking for Package Vulnerabilities

To check for known vulnerabilities in your installed packages:

```sh
pip-audit
```

First, you'll need to install `pip-audit` if you haven't already:

```sh
pip install pip-audit
```