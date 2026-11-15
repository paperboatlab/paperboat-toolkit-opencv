opencv
======

The optional image-processing toolkit for Paperboat: classic image stages on ``image`` wires, an
``Image`` station object, an ``image`` instrument for the Board, and three examples. It depends on
OpenCV and is kept out of the core engine so the main build stays light.

.. toctree::
   :maxdepth: 1

   install
   examples
   blocks/index

Every image stage takes ``image`` in and gives ``image`` out unless it says otherwise. Pure stages
are cacheable; ``save`` and ``background`` are not.

.. list-table::
   :header-rows: 1

   * - Group
     - Blocks
   * - Geometry
     - ``resize``, ``crop``, ``flip``, ``rotate``
   * - Colour and tone
     - ``gray``, ``convert``, ``normalize``, ``equalize``, ``clahe``
   * - Filters and edges
     - ``blur``, ``median``, ``threshold``, ``adaptive_threshold``, ``hsv_range``, ``canny``, ``sobel``,
       ``laplacian``, ``erode``, ``dilate``, ``open``, ``close``, ``invert``, ``distance``
   * - Image algebra
     - ``bitwise``, ``blend``, ``absdiff``, ``background``
   * - Analysis
     - ``stats``, ``centroid``, ``contours``, ``hough_lines``, ``hough_circles``, ``template_match``
   * - Annotation and output
     - ``draw``, ``save``
   * - Instrument
     - ``view`` (the ``image`` instrument on the Board)
   * - Station object
     - ``image`` (a picture from a ``file`` prop; its linked block outputs it)
