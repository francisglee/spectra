# Spectra

> Spectra is a Python library that contains tools to process spectral data.

This repository contains research and implementation of spectral analysis. The first focus will be on preprocessing of LC/MS spectral data; the goal, however, is to include tools for all spectrometry and spectroscopy spectral analysis techniques.

---

## Table of Contents

1.  [Introduction](#introduction)
2.  [Getting Started](#getting-started)
3.  [Development Setup](#development-setup)
4.  [Usage Examples](#usage-examples)
5.  [Release History](#release-history)
6.  [Contributing](#contributing)

---

## Introduction

I'm interested in building a tool that automates algorithm selection for spectral analysis. Popular tools such as [OpenMS](link) and [MZMine2](link) have put alot of work into building functional code to perform many tasks in, for example, Mass Spectrometry analysis. This effort hopes to stand apart from these works in two respects:

1.  We hope to enable, inform, and empower users by taking a **algorithm-centric** approach to analysis. As certain algorithms become commonplace, we place ourselves in danger by using algorithms that are widely adopted, which may not hone our algorithm intuition.
2.  We hope to automate inference on algorithm selection in order to scale process operations. Most algorithms are evaluated by visual inspection. Some use error models such as RMSE, but these strategies cannot discriminate artifacts from desired signals.

On an aside, I'm a big fan of Python, and can speak to [increased productivity](https://murillogroupmsu.com/numba-versus-c/) with Python development. As these modules mature, the Python implementations should be converted to [jit](https://en.wikipedia.org/wiki/Just-in-time_compilation) using Python's [numba](https://numba.pydata.org/) package, and further optimized in C++. This work thus starts the exploration in Python.

Have a look at the [documentation](./docs/README.md) for more information on the algorithmic code, and take a look at the web application, [spectra](website-link), to see performance of various algorithms.

---

## Getting Started

### Requirements

1.  Python 3.6.4+

### Installation

1.  Clone the `spectra` repository.

    ```bash
    $ git clone --recursive https://www.github.com/francisglee/spectra
    ```

1.  Create and activate virtual environment.

    ```bash
    $ cd spectra
    $ python3.6 -m venv .venv
    $ source .venv/bin/activate
    ```

1.  Install requirements.

    ```bash
    (.venv)$ pip install -r requirements.txt
    ```

1.  Install environment onto Jupyter.

    ```bash
    (.venv)$ python3.6 -m ipykernel install --user --name=venv
    ```

1.  Run Juypter notebook.

    ```bash
    (venv)$ jupyter notebook
    ```

---

## Development Setup

### Running Tests

---

## Usage Examples

---

## Release History

We use SemVer for versioning. For the versions available, see the tags on this repository.

2.0.0 -
1.1.0 -
1.0.0 - 

---

## Contributing

### Authors

### Built With

---

## TODO

1.  