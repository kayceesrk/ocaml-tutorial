# OCaml Tutorial

This repository contains exercises and build instructions for the OCaml tutorial
run at [Abstraction 2019](https://abstraction-iitm.surge.sh/#schedule) held at
IIT Madras on April 21st 2019.

## Setup

### Docker Setup

A docker image is available if you do not wish to set up locally. This works
everywhere that docker works.

```bash
$ git clone https://github.com/kayceesrk/ocaml-tutorial
$ cd ocaml-tutorial/notebooks
$ docker run -p 8888:8888 -v `pwd`:/notebooks kayceesrk/ocaml-tutorial-q2_2019:latest
```

Copy and paste the URL displayed into your browser. If you save the changes to
the notebook, they are saved locally. In order to terminate the container, do

```bash
$ docker kill `docker ps -l -q`
```

Assuming this is the latest container.

### Setup locally

These instructions should work on Linux and MacOS. OPAM is OCaml package
manager. On windows, use a Linux VM. The short installation instruction is:


First install the OCaml compiler 4.07.1 and the OPAM package manager. 

```bash
$ sh <(curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh)
$ opam init
```

The detailed installation instructions are [here](https://opam.ocaml.org/doc/Install.html).

Next install OCaml Jupyter Kernel:

```bash
$ pip install jupyter
$ opam install jupyter
$ jupyter kernelspec install --name ocaml-jupyter "$(opam config var share)/jupyter"
```

`pip` is a package installer for python, whose installation instructions are
available [here](https://pypi.org/project/pip/).

The exercises are in `notebooks` directory. In order to start a jupyter session:

```bash
$ git clone https://github.com/kayceesrk/ocaml-tutorial
$ cd ocaml-tutorial/notebooks
$ jupyter notebook
```

This should open up a Jupyter session in our browser.
