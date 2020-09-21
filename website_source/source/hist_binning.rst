=======
binning
=======

.. function:: bin_data(data[, minimum=None, maximum=None, bin_size=None, bin_number=100, normalised=True])

    Returns the (normalised) number count of a data set with values within defined bins.

    :param data: Data.
    :type data: array
    :param minimum: Minimum value for the histogram bins.
    :type minimum: float
    :param maximum: Maximum value for the histogram bins.
    :type maximum: float
    :param bin_size: Size of the bins.
    :type bin_size: float
    :param bin_number: Number of bins.
    :type bin_number: int
    :param normalised: If ``True`` the histogram will be normalised.
    :type normalised: bool

    :returns:
      * **bin_centres** *(array)*: The central value of each bin.
      * **binned_data** *(array)*: The binned number count (or normalised histogram) of the data set.
