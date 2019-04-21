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
$ docker run -it -p 8888:8888 -v `pwd`:/notebooks kayceesrk/ocaml-tutorial-q2_2019:latest
$ jupyter notebook --ip=0.0.0.0
```

Copy and paste the URL displayed into your browser. If you save the changes to
the notebook, they are saved locally. 

### Setup locally

These instructions should work on Linux and MacOS. OPAM is OCaml package
manager. On windows, use a Linux VM. The short installation instruction is:

First install the OCaml compiler 4.07.1 and the OPAM package manager. 

```bash
$ sh <(curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh)
$ opam init
```

The detailed installation instructions are
[here](https://opam.ocaml.org/doc/Install.html). Then install required packages:

```bash
$ pip install jupyter
$ opam -y depext lwt_ssl
$ opam install -y lwt_ssl merlin utop user-setup github-unix jupyter
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

## Acknowledgements

The exercises are generously borrowed from other OCaml tutorials

* JaneStreet & OCaml Labs [learn OCaml workshop](https://github.com/ocamllabs/learn-ocaml-workshop)
* OCaml Labs [2048 tutorial](https://github.com/ocamllabs/2048-tutorial)
