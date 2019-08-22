
Introduction
------------

MiSTree is designed with the intent of being an easy to use minimum spanning tree
library. The methods and statistics used in the module are discussed in the paper
**"Beyond two-point statistics: using the Minimum Spanning Tree as a tool for cosmology"**
[ArXiv=1907.00989] which can be found `here <https://arxiv.org/abs/1907.00989>`_.

.. image:: https://zenodo.org/badge/170473458.svg
   :target: https://zenodo.org/badge/latestdoi/170473458

Dependencies
------------

You will need the following python modules:

* `numpy <http://www.numpy.org/>`_
* `scipy <https://scipy.org/>`_
* `scikit-learn <http://scikit-learn.org/stable/>`_
* `f2py <https://docs.scipy.org/doc/numpy/f2py/>`_ (should be installed with numpy)

If ``f2py`` cannot find a ``gcc`` compiler then the fortran modules will not compile.
If you have this issue and are using an anaconda distribution of python then you
should be able to install ``gcc`` directly using the commands::

    conda install -c anaconda gcc

The module has been tested on Python version 2.7, 3.5 and 3.7.

Installation
------------

To use MiSTree you must first download the package from `github
<https://github.com/knaidoo29/mistree>`_. Using a terminal go into the MiSTree
directory and run::

   python setup.py

This will compile a set of fortran subroutines which are called by MiSTree. If they are
compiled correctly you should see a message of the form::

   Check whether the fortran files have compiled.
   'fortran file 1' ... Yes
    ...
   'fortran file N' ... Yes

Assuming these compile correctly you will then need to add the MiSTree directory
to your python path.

.. note::
    If you're using a mac you would add this to your ``.bash_profile`` file (a hidden file
    located in your home folder):

    ``export PYTHONPATH=$PYTHONPATH:<path/to/mistree>``

    Then run ``source .bash_profile``.

Once this is done you should be able to call MiSTree from python:

.. code-block:: python

   import mistree as mist

Contents
--------

.. toctree::
   :maxdepth: 3

   levy_flight
   minimum_spanning_tree

Version History
---------------

**Version 1**:

   * Constructing the MST of an input data set:

      - 2D, 3D, tomographic or spherical polar coordinates.
      - Apply scale cuts.

   * Analysis routines for the MST:

      - Measures the degree, edge length, branch length and branch shape of the constructed MST.

   * Constructs random walk distribution with :

      - Lévy flight.
      - Adjusted Lévy flight.
      - User defined random walk distribution.
      - In 2D/3D and with/without periodic boundary conditions.

Support
-------

If you have any issues with the code or would like to suggest ways of improving
it, feel free to e-mail:

- krishna.naidoo.11@ucl.ac.uk
