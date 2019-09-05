========
plotting
========

.. function:: set_plot_default([use_bold=True])

    Sets the default fonts for the matplotlib plots.

    :param use_bold: Determines whether the fonts used are in bold.
    :type use_bold: bool

.. function:: plot_histogram_line(x_min, histogram[, x_edges=None, ax=None, color='C0', alpha=1., linewidth=1., linestyle='-'])

    Outputs the histogram line boxes without using the histogram function.

    :param x_mid: Midpoint of each histogram bar.
    :type x_mid: array
    :param histogram: Histogram height.
    :type histogram: array
    :param x_edges: The edges of each histogram bar. Ideal for unequal spacings between histograms.
    :type x_edges: array
    :param ax: The matplotlib plotting axis.
    :type ax: class
    :param color: The color of the histogram error plot.
    :type color: str
    :param alpha: The transparency fraction of the histogram error plot.
    :type alpha: float
    :param linewidth: The linewidth of histogram line.
    :type linewidth: float
    :param linestyle: The linestyle used.
    :type linestyle: str

.. function:: plot_histogram_confidence(x_mid, histogram_min, histogram_max[, x_edges=None, ax=None, color='C0', alpha=0.25])

    Plots the confidence envelopes for a histogram.

    :param x_mid: Midpoint of each histogram bar.
    :type x_mid: array
    :param histogram_min: Histogram minimum envelope.
    :type histogram_min: array
    :param histogram_max: Histogram maximum envelope.
    :type histogram_max: array
    :param x_edges: The edges of each histogram bar. Ideal for unequal spacings between histograms.
    :type x_edges: array
    :param ax: The matplotlib plotting axis.
    :type ax: class
    :param color: The color of the histogram error plot.
    :type color: str
    :param alpha: The transparency fraction of the histogram error plot.
    :type alpha: float

.. function:: plot_histogram_error(x_mid, histogram, histogram_error[, x_edges=None, ax=None, color='C0', alpha=0.25])

    :param x_mid: Midpoint of each histogram bar.
    :type x_mid: array
    :param histogram: Histogram.
    :type histogram: array
    :param histogram_error: The error associated to each histogram bar.
    :type histogram_error: array
    :param x_edges: The edges of each histogram bar. Ideal for unequal spacings between histograms.
    :type x_edges: array
    :param ax: The matplotlib plotting axis.
    :type ax: class
    :param color: The color of the histogram error plot.
    :type color: str
    :param alpha: The transparency fraction of the histogram error plot.
    :type alpha: float
