.. _README:

.. image:: https://coveralls.io/repos/github/metno/pysurfex/badge.svg?branch=master


Python API to SURFEX (pysurfex)
=======================================================

An API in python to the external surface model SURFEX.
    - Prepare input and namelists to a SURFEX binary
    - Create atmospheric forcing for offline SURFEX runs
    - Read SURFEX output
    - A scheduler setup to run offline SURFEX experiments
    - Quality control of observations with titanlib
    - Optimal interpolation with gridpp
    - Monitor the observations usage

See online documentation in https://metno.github.io/pysurfex/

Installation on debian based Linux system
--------------------------------------------

Install the required pacakges:

.. code-block:: bash

  sudo apt-get update
  # Python tools
  sudo apt-get install python3-setuptools python3-numpy python3-scipy
  # Cfunits
  sudo apt-get install libudunits2-dev
  # Titanlib
  sudo apt-get install libboost-dev libproj-dev libarmadillo-dev libgsl-dev

The following depencies are needed. Install the non-standard ones e.g. with pip or your system installation system.

General dependencies
---------------------

.. code-block:: bash

  numpy
  scipy
  netCDF4
  cfunits
  pyproj
  pyyaml
  toml
  tomlkit
  netCDF4
  jsonmerge
  datetime
  f90nml
  enum34
  requests
  json; python_version < '3'
  StringIO; python_version < '3'
  eccodes
  db-sqlite3

To read NetCDF files:

.. code-block:: bash

  NetCDF4

To read grib files:

.. code-block:: bash

  eccodes

from ECMWF https://software.ecmwf.int/wiki/display/ECC/Releases installed with ENABLE_PYTHON=ON

To plot:

.. code-block:: bash

  matplotlib
  cartopy

To get observations from frost.met.no API:

.. code-block:: bash

  requests

For Quality control of observations

.. code-block:: bash

  titanlib

For optimal interpolation and observation operators

.. code-block:: bash

  gridpp

For testing:

.. code-block:: bash

  unittest
  nose
  Testdata from https://drive.google.com/open?id=1CCcKqRUp7fwZKGzWHXMjBxaXKVWWQiTO

Download the source code, then install ``pysurfex`` by executing the following inside the extracted
folder:

Install pysurfex
-------------------------------------------
.. code-block:: bash

  sudo pip install -e .


Create documentation
---------------------------------------------

.. code-block:: bash

  cd docs
  # Create html documentation
  make html
  # Create latex documentation
  make latex
  # Create a pdf documentation
  make latexpdf


Examples
-----------------------

.. include:: docs/example.rst


