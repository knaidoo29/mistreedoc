=======
binning
=======

.. function:: bin_data(data[, minimum=None, maximum=None, bin_size=None, bin_number=100, normalised=True])

    Returns the (normalised) number count of a data set with values within defined bins.

    :param data:
    :type data: array
    :param minimum:
    :type minimum: float
    :param maximum:
    :type maximum: float
    :param bin_size:
    :type bin_size: float
    :param bin_number:
    :type bin_number: int
    :param normalised:
    :type normalised:

    :returns:
      * **bin_centres** *(array)*: The central value of each bin.
      * **binned_data** *(array)*: The binned number count (or normalised histogram) of the data set.
