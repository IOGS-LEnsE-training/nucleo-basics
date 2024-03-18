External ressources / libraries
###############################

The MBED community being an **active and growing** community, a **large number of libraries** are developed and made available by their creators.

LEnsE ressources
****************

The **LEnsE** team develops **ressources** (libraries and examples) for Mbed-OS. These ressources are accessible in this repository: `MBED6 Libraries <https://iogs-lense-ressources.github.io/mbed6-libraries/>`_.

.. figure:: ../_static/images/lense_mbed6_libs.png
	:align: center	
	:width: 50%
	
	MBED6 Libraries repository snap.


To use these ressources you have to follow these steps:

#. Download all the .h and .cpp files from the library. See `Download files from a GitHub Repository <https://lense.institutoptique.fr/github/#download-files-from-a-github-repository>`_ . (often in the libs directory).
#. Create a project in Keil Studio Cloud (or MBED Studio) based on the version 6 of MBED - Blinky baremetal. See :ref:`Creation of a MBED project <mbed_project>`.
#. Create a :file:`libs` directory in your project.
#. Copy all the downloaded files into this directory.
#. Download and copy the example contained in the :file:`main_xxx.cpp` file.
#. Compile and test the code on a suitable Nucleo board.

You must first have connected the component you want to control to the Nucleo board, following the inputs and outputs recommended by the example.



External ressources
*******************

