---
title: "My First Post"
date: 2023-05-29T16:11:29+09:00
draft: true
tags: ["outline", "dev"]
cover:
    image: "https://www.google.com/url?sa=i&url=https%3A%2F%2Funsplash.com%2Fs%2Fphotos%2Fpretty&psig=AOvVaw1S8ZLicgFTxE-lQQ2JgDTm&ust=1685610650592000&source=images&cd=vfe&ved=0CBEQjRxqFwoTCLCi-ZGbn_8CFQAAAAAdAAAAABAE" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
---

Creating a new environment with **venv** (preferred)

```shell
python3 -m venv <env_name>   # env_name usually venv
```

Creating a new environment with **virtualenv**:

```shell
python3 -m pip --version  # check if pip is installed
python3 -m pip install --user -U virtualenv  # Install virtualenv tool
cd path-to-project
virtualenv <env_name>  # Create enviroment
```

By default, this will create an environment with all the packages available "system-wide".
Export environment:

``` shell
pip freeze > requirements.txt
```

Recreate environment:

```shell
$ virtualenv <env_name>
$ source <env_name>/bin/activate
(<env_name>)$ pip install -r path/to/requirements.txt
```

Source: [How to export virtualenv?](https://stackoverflow.com/questions/14684968/how-to-export-virtualenv), from stackoverflow

What's the difference between `virtualenv <env_name>` and `python3 -m venv <env_name>`?

> **venv**: It's the Python 3.3+ [stdlib package](https://docs.python.org/3/library/venv.html) whose purpose was to improve and replace the PyPi [virtualenv package](https://pypi.python.org/pypi/virtualenv) (see [PEP 405](https://www.python.org/dev/peps/pep-0405/)). But it seems it's not there yet (at least not as feature-complete). (*[source](https://askubuntu.com/questions/603935/pyvenv-vs-venv-vs-python-virtualenv-vs-virtualenv-and-python-3)*)

> virtualenv is a tool to create isolated Python environments. Since Python 3.3, a subset of it has been integrated into the standard library under the [venv module](https://docs.python.org/3/library/venv.html). The venv module does not offer all features of this library ... ([_source_](https://virtualenv.pypa.io/en/latest/))
