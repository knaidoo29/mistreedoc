===========
PlotHistMST
===========

.. class:: PlotHistMST()

    A class for plotting the MST statistics.

    .. function:: read_mst(mst_hist[, color=None, linewidth=2., linestyle=None, alpha=0.8, label=None, alpha_envelope=0.3])

        Input MST statistics.

        :param mst_hist: Binned MST dictionary given in the format outputted by HistMST.
        :type mst_hist: dict
        :param color: Color of the MST histogram.
        :type color: str
        :param linewidth: Width of the histogram line used.
        :type linewidth: float
        :param linestyle: Linestyle used.
        :type linestyle: str
        :param alpha: The transparency of the line.
        :type alpha: float
        :param label: label used in the legend, this will only appear in the legend if this is given.
        :type label: str
        :param alpha_envelope: The transparency of envelopes (usually the standard deviation of the counts in each bin).
        :type alpha_envelope: float

    .. function:: plot([usebox=True, saveas=None, fontsize=16, figsize=(16, 4), subplot_setup='4x1', units=None, showenvelopes=True, showsigma=2, usecomp=True, usemean=False, heigh_ratios=[2, 1], usefraction=True, whichcomp=0, plotzeroline=True, legend=True, subplot_adjust_top=0.85, legend_fontsize=14, legend_column=4, xlabels=[None, None, None, None], dpi=None, plt_output='show'])

        Outputs the final plot of the MST statistics.

        :param usebox: For l, b and s this sets whether to use boxes for the histogram or to simple plot as line from the bin centre.
        :type usebox: bool
        :param saveas: If not None, this will save the plot with the name provided.
        :type saveas: str
        :param fontsize: Fontsize of axis labels.
        :type fontsize: int
        :param figsize: Dimensions of the figure.
        :type figsize: tuple
        :param subplot_setup: Subplot setup: '4x1' or '2x2'.
        :type subplot_setup: str
        :param units: Units of l and b MST statistics, if None is supplied then we assume it is unitless.
        :type units: str
        :param showenvelopes: This determines whether to plot data with input standard deviation.
        :type showenvelopes: bool
        :param showsigma: Number of sigma errorbars to plot.
        :type showsigma: int
        :param usecomp: Determines whether to include comparison subplots.
        :type usecomp: bool
        :param usemean: For comparison plots, the determines whether to use the mean of input distributions.
        :type usemean: bool
        :param height_ratios: Height ratio between main plots and comparison plots.
        :type height_ratios: tuple
        :param usefraction: If true comparison plots are given by the fractional difference to a reference data otherwise they are given as absolute differences.
        :type usefraction: bool
        :param whichcomp: Determines which data should be the reference data that all other data is compared to. Only used if usemean == False.
        :type whichcomp: int
        :param plotzeroline: Plots horizontal zero line for subplot.
        :type plotzeroline: bool
        :param legend: Determines whether to include a legend.
        :type legend: bool
        :param subplot_adjust_top: float
        :type subplot_adjust_top: If legend == True then the figure's top is adjusted by the input value.
        :param legend_fontsize: Size of legend text.
        :type legend_fontsize: int
        :param legend_column: Number of keys in each line of the legend.
        :type legend_column: int
        :param xlabels: List of string labels to replace the default if not set to None.
        :type xlabels: list
        :param dpi: Pixels per inch for non-vector images.
        :type dpi: int
        :param plt_output: output type: 'closed' or 'show'
        :type plt_output: str

    .. function:: clean()

        Resets PlotHistMST variables.
