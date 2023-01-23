---
title: Virtual environment
tags: programming-languages
---

# Virtual environment

A **virtual environment** is a self contained directory tree with its own [[python|Python]] installation of a particular version and any additional packages.

Virtual environments are used to ensure applications are portable across machines, as long as that machine can run and install the required Python version and its packages.

## Creating virtual environments

Creating a virtual environment with the name `my-venv`:

```sh
python3 -m venv my-venv
```

## Running the virtual environment

On Windows:

```sh
my-venv\Scripts\activate.bat
```

On MacOS or Unix:

```sh
source my-venv/bin/activate
```

Deactivating the virtual environment:

```
deactivate
```

You can now install packages with `pip` like normal, but now they will be contained in the virtual environment.

I was able to install packages using `pip install` directly (instead of `python3 -m pip install`), likely due to my `PATH`. Try using the command with or without `python3 -m` and see what works.

## Sources

- <https://docs.python.org/3/tutorial/venv.html>
