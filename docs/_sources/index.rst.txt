
+---------------+-----------------------------------------+
| Author        | Krishna Naidoo                          |
+---------------+-----------------------------------------+
| Version       | 1.2.0                                   |
+---------------+-----------------------------------------+
| Homepage      | https://github.com/knaidoo29/mistree    |
+---------------+-----------------------------------------+
| Documentation | https://knaidoo29.github.io/mistreedoc/ |
+---------------+-----------------------------------------+

.. |br| raw:: html

        <br>

.. image:: https://travis-ci.org/knaidoo29/mistree.svg?branch=master
    :target: https://travis-ci.org/knaidoo29/mistree
.. image:: https://codecov.io/gh/knaidoo29/mistree/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/knaidoo29/mistree
.. image:: https://badge.fury.io/py/mistree.svg
    :target: https://badge.fury.io/py/mistree
.. image:: https://joss.theoj.org/papers/461d79e9e5faf21029c0a7b1c928be28/status.svg
    :target: https://joss.theoj.org/papers/461d79e9e5faf21029c0a7b1c928be28
.. image:: https://zenodo.org/badge/170473458.svg
    :target: https://zenodo.org/badge/latestdoi/170473458
.. image:: https://img.shields.io/badge/License-MIT-blue.svg
    :target: https://opensource.org/licenses/MIT
.. image:: https://mybinder.org/badge_logo.svg
    :target: https://mybinder.org/v2/gh/knaidoo29/mistree/master?filepath=tutorials%2Fnotebooks%2F
.. image:: https://img.shields.io/badge/ascl-1910.016-blue.svg?colorB=262255
    :target: http://ascl.net/1910.016

|br|

Introduction
------------

The Minimum Spanning Tree (MST) has been used in a broad range of scientific research including computer science, epidemiology, social sciences, particle physics, astronomy and cosmology. Its success in these field has been driven by its sensitivity to the spatial distribution of points and the patterns within. MiSTree, a public Python package, allows a user to construct the MST in a variety of coordinates systems, including Celestial coordinates used in astronomy. The package enables the MST to be constructed quickly by initially using a k-nearest neighbour graph (rather than a matrix of pairwise distances) which is then fed to Kruskal's algorithm to construct the MST. MiSTree enables a user to measure the statistics of the MST and provides classes for binning the MST statistics (into histograms) and plotting the distributions. Including the MST in parameter estimation studies in cosmology will enable the inclusion of high-order statistics information from the cosmic web. This information has traditionally been unexploited due to the computational cost of calculating N-point statistics.

Dependencies
------------

MiSTree will work on Python 2.7 or 3.4+ and requires the following Python modules:

* `numpy <http://www.numpy.org/>`_
* `matplotlib <https://matplotlib.org>`_
* `scipy <https://scipy.org/>`_
* `scikit-learn <http://scikit-learn.org/stable/>`_
* `f2py <https://docs.scipy.org/doc/numpy/f2py/>`_ (should be installed with numpy)

For testing you will require `nose <https://nose.readthedocs.io/en/latest/>`_ or `pytest <http://pytest.org/en/latest/>`_ .

Installation
------------

MiSTree can be installed as follows::

    pip install mistree [--user]

The ``--user`` is optional and only required if you don’t have write permission. If you are
using a windows machine this may not work, in this case (or as an alternative to pip) clone the repository::

    git clone https://github.com/knaidoo29/mistree.git
    cd mistree

and install by either running::

    pip install . [--user]

or::

    python setup.py build
    python setup.py install

Similarly, if you would like to work and edit mistree you can clone the `repository <https://github.com/knaidoo29/mistree>`_
and install an editable version::

    git clone https://github.com/knaidoo29/mistree.git
    cd mistree
    pip install -e . [--user]

From the ``mistree`` directory you can then test the install using ``nose``::

    python setup.py test

or using ``pytest``::

    python -m pytest

Once this is done you should be able to call MiSTree from python:

.. code-block:: python

    import mistree as mist

Citing
------

You can cite ``MiSTree`` using the following BibTex::

    @ARTICLE{Naidoo2019,
             author = {{Naidoo}, Krishna},
             title = "{MiSTree: a Python package for constructing and analysing Minimum Spanning Trees}",
             journal = {The Journal of Open Source Software},
             year = "2019",
             month = "Oct",
             volume = {4},
             number = {42},
             eid = {1721},
             pages = {1721},
             doi = {10.21105/joss.01721},
             adsurl = {https://ui.adsabs.harvard.edu/abs/2019JOSS....4.1721N}
    }

Support
-------

If you have any issues with the code or want to suggest ways to improve it please
open a new issue (`here <https://github.com/knaidoo29/mistree/issues>`_)
or (if you don't have a github account) email krishna.naidoo.11@ucl.ac.uk.

Contents
--------

.. toctree::
   :maxdepth: 3

   levy_flight
   minimum_spanning_tree

Version History
---------------

**Version 1.0**:

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

**Version 1.1**:

    * Added binning (``HistMST``) and plotting (``PlotHistMST``) classes for handling the MST statistics.

**Version 1.2**:

    * Added automated testing routines which can be executed using `nose` or `pytest`.
