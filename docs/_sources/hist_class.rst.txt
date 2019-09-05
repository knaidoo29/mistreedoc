=======
HistMST
=======

.. class:: HistMST()

    A class for binning the default MST statistics which are then stored in a dictionary.

    .. function:: setup([uselog=False, use_sqrt_s=True, usenorm=True, d_min=0.5, d_max=6.5, num_d_bins=6, l_min=0., l_max=None, num_l_bins=100, b_min=0., b_max=None, num_b_bins=100, s_min=0., s_max=1., num_s_bins=50, logl_min=None, logl_max=None, logb_min=None, logb_max=None])

        Setups bin sizes for the MST statistics.

        :param uselog: Determines whether to use log bins for l and b.
        :type uselog: bool
        :param use_sqrt_s: Determines whether to use the sqrt(1-s) projection of s or just s itself.
        :type use_sqrt_s: bool
        :param usenorm: Determines whether to normalise the histograms.
        :type usenorm: bool
        :param d_min: Minimum for degree bins (use half integer values).
        :type d_min: float
        :param d_max: Maximum for degree bins (use half integer values).
        :type d_max: float
        :param num_d_bins: Number of bins for the distribution of degree, this should be equal to d_max - d_min.
        :type num_d_bins: int
        :param l_min: Minimum for edge length bins.
        :type l_min: float
        :param l_max: Maximum for edge length bins.
        :type l_max: float
        :param num_l_bins: Number of bins for the distribution of edge lengths.
        :type num_l_bins: int
        :param b_min: Minimum for branch length bins.
        :type b_min: float
        :param b_max: Maximum for branch length bins.
        :type b_max: float
        :param num_b_bins: Number of bins for the distribution of branch lengths.
        :type num_b_bins: int
        :param s_min: Minimum for branch shape bins.
        :type s_min: float
        :param s_max: Maximum for branch shape bins.
        :type s_max: float
        :param num_s_bins: Number of bins for the distribution of branch shapes.
        :type num_s_bins: int
        :param logl_min: Minimum of edge lengths in log to base 10.
        :type logl_min: float
        :param logl_max: Maximum of edge lengths in log to base 10.
        :type logl_max: float
        :param logb_min: Minimum of branch lengths in log to base 10.
        :type logb_min: float
        :param logb_max: Maximum of branch lengths in log to base 10.
        :type logb_max: float

    .. function:: get_hist(d, l, b, s)

        Bins the MST distribution which is returned as a dictionary.

        :param d: Distribution of degree.
        :type d: array
        :param l: Distribution of edge length.
        :type l: array
        :param b: Distribution of branch length.
        :type b: array
        :param s: Distribution of branch shape.
        :type s: array

        :returns: **mst_hist** *(dict)*: Dictionary of MST binned histograms.

    .. function:: start_group()

        Begins group mode for calculating the mean and standard deviation of the MST from different realisations of data points coming from the same model.

    .. function:: end_group()

        Ends group mode for calculating the mean and standard deviation of the MST.

        :returns: **mst_hist** *(dict)*: Dictionary of the mean and standard deviation of the MST binned histograms.

    .. function:: clean()

        Resets HistMST variables.
