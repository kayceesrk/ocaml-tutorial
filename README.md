# OCaml Tutorial

This repository contains exercises and build instructions for the OCaml tutorial
run at [Abstraction 2019](https://abstraction-iitm.surge.sh/#schedule) held at
IIT Madras on April 21st 2019.

## Setup

You will need a machine that can run Linux or MacOS.

### Install OPAM

OPAM is OCaml package manager. The short installation instruction is:

```bash
$ sh <(curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh)
$ opam init
```

This should install the OCaml compiler 4.07.1 and the OPAM package manager. The
detailed installation instructions are
[here](https://opam.ocaml.org/doc/Install.html).

### Install OCaml Jupyter Kernel

We will use OCaml Jupyter Kernel for our exercises. This can be installed with:

```bash
$ pip install jupyter
$ opam install jupyter
$ jupyter kernelspec install --name ocaml-jupyter "$(opam config var share)/jupyter"
```

`pip` is a package installer for python, whose installation instructions are
available [here](https://pypi.org/project/pip/).
