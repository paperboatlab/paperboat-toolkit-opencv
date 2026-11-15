Examples
========

Three complete backends ship with the toolkit, named ``ocv-NN-<topic>`` so they are easy to tell
apart from the numbered tutorials:

.. list-table::
   :header-rows: 1

   * - Example
     - Port
     - Shows
   * - ``ocv-01-parts-counter``
     - 8781
     - A synthetic conveyor, threshold and morphology, ``contours`` and ``draw``
   * - ``ocv-02-shape-inspector``
     - 8782
     - ``hough_circles`` and ``contours`` on one test card
   * - ``ocv-03-image-lab``
     - 8783
     - ``resize``, ``crop``, ``equalize``, ``sobel`` and ``stats``

The installer copies them next to the toolkit; the CLI lists and starts them like any other
backend:

.. code-block:: sh

   paperboat toolkit install opencv
   paperboat backends
   paperboat run ocv-01
