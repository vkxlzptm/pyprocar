
.. DO NOT EDIT.
.. THIS FILE WAS AUTOMATICALLY GENERATED BY SPHINX-GALLERY.
.. TO MAKE CHANGES, EDIT THE SOURCE PYTHON FILE:
.. "examples\01-dos\plotting_noncolinear_dos_qe.py"
.. LINE NUMBERS ARE GIVEN BELOW.

.. only:: html

    .. note::
        :class: sphx-glr-download-link-note

        Click :ref:`here <sphx_glr_download_examples_01-dos_plotting_noncolinear_dos_qe.py>`
        to download the full example code

.. rst-class:: sphx-glr-example-title

.. _sphx_glr_examples_01-dos_plotting_noncolinear_dos_qe.py:


.. _ref_plotting_noncolinear_dos_qe:

Plotting non colinear dos in Quantum Espresso
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Plotting non colinear dos in Quantum Espresso.

First download the example files with the code below. Then replace data_dir below.

.. code-block::
   :caption: Downloading example

    data_dir = pyprocar.download_example(save_dir='', 
                                material='Fe',
                                code='qe', 
                                spin_calc_type='non-colinear',
                                calc_type='dos')

.. GENERATED FROM PYTHON SOURCE LINES 23-24

importing pyprocar and specifying local data_dir

.. GENERATED FROM PYTHON SOURCE LINES 24-32

.. code-block:: default

    import os
    import pyprocar


    project_dir = os.path.dirname(os.path.dirname(os.getcwd()))
    data_dir = f"{project_dir}{os.sep}data{os.sep}examples{os.sep}Fe{os.sep}qe{os.sep}non-colinear{os.sep}dos"









.. GENERATED FROM PYTHON SOURCE LINES 33-41

Parametric mode
+++++++++++++++++++++++++++++++++++++++
Quantum Espresso expresses the projections in the coupled basis, 
therefore orbitals takes different meanings.
For details on the meaning of the indices of the atomic projection please refer to the user guide :ref:'atomic_projections'




.. GENERATED FROM PYTHON SOURCE LINES 41-53

.. code-block:: default

    atoms=[0]
    spins=[0]
    orbitals=[8,9,10,11,12,13,14,15,16,17]

    pyprocar.dosplot(
                    code='qe', 
                    mode='parametric',
                    atoms=atoms,
                    orbitals=orbitals,
                    spins=spins,
                    vmin=0,
                    vmax=1,
                    dirname=data_dir)


.. image-sg:: /examples/01-dos/images/sphx_glr_plotting_noncolinear_dos_qe_001.png
   :alt: plotting noncolinear dos qe
   :srcset: /examples/01-dos/images/sphx_glr_plotting_noncolinear_dos_qe_001.png
   :class: sphx-glr-single-img


.. rst-class:: sphx-glr-script-out

 .. code-block:: none


    <pyprocar.plotter.dos_plot.DOSPlot object at 0x000001E20AE25B50>




.. rst-class:: sphx-glr-timing

   **Total running time of the script:** ( 0 minutes  19.153 seconds)


.. _sphx_glr_download_examples_01-dos_plotting_noncolinear_dos_qe.py:

.. only:: html

  .. container:: sphx-glr-footer sphx-glr-footer-example


    .. container:: sphx-glr-download sphx-glr-download-python

      :download:`Download Python source code: plotting_noncolinear_dos_qe.py <plotting_noncolinear_dos_qe.py>`

    .. container:: sphx-glr-download sphx-glr-download-jupyter

      :download:`Download Jupyter notebook: plotting_noncolinear_dos_qe.ipynb <plotting_noncolinear_dos_qe.ipynb>`


.. only:: html

 .. rst-class:: sphx-glr-signature

    `Gallery generated by Sphinx-Gallery <https://sphinx-gallery.github.io>`_
