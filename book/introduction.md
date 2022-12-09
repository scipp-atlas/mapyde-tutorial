# `mapyde` Tutorial

## Welcome!

<p align="center">
<a href="https://github.com/scipp-atlas/mario-mapyde"><img src="https://raw.githubusercontent.com/scipp-atlas/mario-mapyde/main/docs/assets/images/logo.svg" alt="Mapyde logo" width="300" role="img" align="left" hspace="25">
</a>
</p>

Welcome to the `mapyde` tutorial!
We'll first point you towards our documentation website ([scipp-atlas.github.io/mario-mapyde](https://scipp-atlas.github.io/mario-mapyde/)) and recommend that you visit it for much more detailed explanations and examples.
Let's dive right in.


We won't review the full pedagogy of the various tools that we can run with `mpayde` which include:
* [MadGraph](https://launchpad.net/mg5amcnlo) (and [Pythia](https://pythia.org/) and MadSpin)
* [Delphes](https://cp3.irmp.ucl.ac.be/projects/delphes)
* [SimpleAnalysis](https://simpleanalysis.docs.cern.ch/)
* [pyhf](https://pyhf.readthedocs.io/)

So please refer to the corresponding tool's documentation for its usage.

Instead, let's move to looking at the `mapyde` CLI right away.

## Installation

### Make a Virtual Environment

````{tabbed} Locally
```
$ python3 -m venv mapyde-tutorial
$ source mapyde-tutorial/bin/activate
(mapyde-tutorial) $ python -m pip install -U pip setuptools wheel
```
````

````{tabbed} On CC7 lxplus/tier-3

First we need to set up the 'views' with the right paths to ensure we use the correct `pip`

```
$ export ATLAS_LOCAL_ROOT_BASE=/cvmfs/atlas.cern.ch/repo/ATLASLocalRootBase
$ source $ATLAS_LOCAL_ROOT_BASE/user/atlasLocalSetup.sh
$ lsetup "views LCG_98python3 x86_64-centos7-gcc8-opt"
$ export PYTHONPATH=/cvmfs/sft.cern.ch/lcg/views/LCG_98python3/x86_64-centos7-gcc8-opt/python:/cvmfs/sft.cern.ch/lcg/views/LCG_98python3/x86_64-centos7-gcc8-opt/lib
```

Then we can go ahead and create the virtual environment

```
$ python3 -m venv mapyde-tutorial
$ source mapyde-tutorial/bin/activate
(mapyde-tutorial) $ python -m pip install -U pip setuptools wheel
```
````

````{tabbed} On SLC6 lxplus/tier-3

First we need to set up the 'views' with the right paths to ensure we use the correct `pip`

```
$ export ATLAS_LOCAL_ROOT_BASE=/cvmfs/atlas.cern.ch/repo/ATLASLocalRootBase
$ source $ATLAS_LOCAL_ROOT_BASE/user/atlasLocalSetup.sh
$ lsetup "views LCG_98python3 x86_64-slc6-gcc8-opt"
$ export PYTHONPATH=/cvmfs/sft.cern.ch/lcg/views/LCG_98python3/x86_64-slc6-gcc8-opt/python:/cvmfs/sft.cern.ch/lcg/views/LCG_98python3/x86_64-slc6-gcc8-opt/lib
```

Then we can go ahead and create the virtual environment

```
$ python3 -m venv mapyde-tutorial
$ source mapyde-tutorial/bin/activate
(mapyde-tutorial) $ python -m pip install -U pip setuptools wheel
```
````

Once you have a virtual environment set up, you can use `source mapyde-tutorial/bin/activate` to get back into it again. Note the prefix `(mapyde-tutorial) $` on your command line, which indicates that you're inside a virtual environment named 'mapyde-tutorial'.

### Getting mapyde

If you haven't already, make a new Python 3 virtual environment and then install `mapyde` from either [PyPI](https://pypi.org/project/mapyde/) with `pip`

```
(mapyde-tutorial) $ python -m pip install mapyde
```

 or [Conda-forge](https://anaconda.org/conda-forge/mapyde)

```
(mapyde-tutorial) $ conda config --add channels conda-forge
(mapyde-tutorial) $ conda install mapyde
```

### Dependencies for this tutorial

To get all the dependencies needed for this tutorial you can just install from the included `requirements.txt` in the top level `binder/` directory of [the source repository](https://github.com/scipp-atlas/mapyde-tutorial)

```
(mapyde-tutorial) $ python -m pip install -r binder/requirements.txt
```

If you want to also get the dependencies to build and explore the Jupyter Book form of the tutorial you can install them with

```
(mapyde-tutorial) $ python -m pip install -r book/requirements.txt
```

### Questions and Further Information on `mapyde`

For more information on `mapyde` please check the [documentation website](https://scipp-atlas.github.io/mario-mapyde).
Additionally, if you have a question about the use of `mapyde` not covered in the documentation, please ask a question the `mapyde` [GitHub Discussions](https://github.com/scipp-atlas/mario-mapyde/discussions).
If you believe you have found a bug in `mapyde`, please report it in the [GitHub Issues](https://github.com/scipp-atlas/mario-mapyde/issues/new?template=Bug-Report.md&labels=bug&title=Bug+Report+:+Title+Here).
