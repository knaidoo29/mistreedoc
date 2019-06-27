==================
coordinate_utility
==================

.. function:: spherical_2_cartesian(r, phi, theta[, units='degree'])

    Converts spherical polar coordinates into cartesian coordinates.

    :param r: Radial distance.
    :type r: array
    :param phi: Longitudinal coordinates.
    :type phi: array
    :param theta: Latitude coordinates.
    :type theta: array
    :param units: Units of ``phi`` and ``theta`` given in either 'degrees' or 'radians'.
    :type units: str

    :returns: **x, y, z** *(array)* : cartesian coordinates.

.. function:: celestial_2_cartesian(r, ra, dec[, units='degree', output='both'])

    Converts celestial spherical polar coordinates into cartesian coordinates.

    :param r: Radial distance.
    :type r: array
    :param ra: Longitudinal celestial coordinates.
    :type ra: array
    :param dec: Latitude celestial coordinates.
    :type dec: array
    :param units: Units of ``ra`` and ``dec`` given in either 'degrees' or 'radians'.
    :type units: str
    :param output: 'euclidean' or 'both'. Determines whether to output only the euclidean or both euclidean and spherical coordinates.
    :type output: str

    :returns: Returns tuple of either:

        * **phi, theta** *(array)* -- 'spherical': spherical polar coordinates.
        * **x, y, z** *(array)* -- 'cartesian': cartesian coordinates.

.. function:: spherical_2_unit_sphere(phi, theta[, units='degrees'])

    Project coordinates on a sphere into cartesian coordinates on a unit sphere.

    :param r: Radial distance.
    :type r: array
    :param phi: Longitudinal coordinates.
    :type phi: array
    :param theta: Latitude coordinates.
    :type theta: array
    :param units: Units of ``ra`` and ``dec`` given in either 'degrees' or 'radians'.
    :type units: str

    :returns: **x, y, z** *(array)* : cartesian coordinates.


.. function:: celestial_2_unit_sphere(ra, dec[, units='degrees', output='both'])

    Project celestial coordinates on a sphere into cartesian coordinates on a unit sphere.

    :param r: Radial distance.
    :type r: array
    :param ra: Longitudinal celestial coordinates.
    :type ra: array
    :param dec: Latitude celestial coordinates.
    :type dec: array
    :param units: Units of ``ra`` and ``dec`` given in either 'degrees' or 'radians'.
    :type units: str
    :param output: 'euclidean' or 'both'. Determines whether to output only the euclidean or both euclidean and spherical coordinates.
    :type output: str

    :returns: Returns tuple of either:

        * **phi, theta** *(array)* -- 'spherical': spherical polar coordinates.
        * **x, y, z** *(array)* -- 'cartesian': cartesian coordinates.

.. function:: perpendicular_distance_2_angle(distance)

    Converts distances on a unit sphere to angular distances projected across a unit sphere.

    :param distance: Perpendicular distances across (i.e. going on the surface) of a unit sphere.
    :type distance: array

    :returns: **angular_distance** *(array)* -- The angular distance of points across a unit sphere.
