Introduction
------------

MiSTree is designed with the intent of being an easy to use minimum spanning tree
library. The methods and statistics used in the module are discussed in the paper
**"Beyond two-point statistics: using the Minimum Spanning Tree as a tool for cosmology"**
[ArXiv=1907.00989] which can be found `here <https://arxiv.org/abs/1907.00989>`_.

Dependencies
------------

You will need the following python modules:

* Python 2.7 or 3.5+
* `numpy <http://www.numpy.org/>`_
* `matplotlib <https://matplotlib.org>`_
* `scipy <https://scipy.org/>`_
* `scikit-learn <http://scikit-learn.org/stable/>`_
* `f2py <https://docs.scipy.org/doc/numpy/f2py/>`_ (should be installed with numpy)

The module has been tested on Python version 2.7, 3.5 and 3.7.

Installation
------------

MiSTree can be installed as follows::

    pip install mistree [--user]

The ``--user`` is optional and only required if you don’t have write permission. If you
want to work on the Github version you can clone the `repository <https://github.com/knaidoo29/mistree>`_
and install it in place::

    git clone https://github.com/knaidoo29/mistree.git
    cd mistree
    pip install -e . [--user]

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

Support
-------

If you have any issues with the code or would like to suggest ways of improving
it, feel free to e-mail:

- krishna.naidoo.11@ucl.ac.uk
