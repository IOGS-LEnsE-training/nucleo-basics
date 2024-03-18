.. _mbed_project:

Creation of a MBED project
##########################

If you want to use MBED Studio, see :ref:`MBED Studio first project <mbed_studio_project>`.

Keil Studio Cloud
*****************

.. note::

	In this section, we assume that you have a MBED account or an Arm® account. See :ref:`Keil Studio Cloud account <keil_studio_cloud>`.


You can access to this platform by following this link: https://www.keil.arm.com/. 

.. figure:: ../_static/images/keil/keil_website.png
	:align: center	

Then click :menuselection:`Keil Studio Cloud`, to access to the login page. Log into the *Keil Studio Cloud* platform with your personal informations.

Keil Studio Cloud IDE
=====================

You will access to the main window of the :abbr:`IDE (Integrated Development Environment)`.

This interface is divided in a classical manner with a **project management** area (on the left side of the interface), a **text editor** area (in the top-right part of the interface) and an **output information** area (in the bottom-right part of the interface).

.. figure:: ../_static/images/keil/keil_cloud_plus.png
	:align: center

	Main window of the Keil Studio Cloud platform. https://www.keil.arm.com/


During your first access, no projects appear in the **project management** part. In this section, you can access to :

* your **personal informations** (icons surrounded by an **orange** border);
* the list of the projects you develop (icon surrounded by a **pink** border).

Create your first project
=========================

To create a new project, you can click :menuselection:`+ New Project` (icon surrounded by a **red** border on the previous figure) or click :menuselection:`File -> New... -> MBED Project`.

.. figure:: ../_static/images/keil/keil_cloud_new_project_mbed.png
	:align: center

	:menuselection:`File -> New... -> MBED Project` in Keil Studio Cloud.

Then select :menuselection:`MBED6 -> mbed-os-example-blinky-baremetal`.

.. figure:: ../_static/images/keil/keil_cloud_new_project_mbed_blinky.png
	:align: center
	:width: 70%
	
	New project selection. 
	
.. warning::

	To avoid any compilation conflicts with other libraries, make sure to select the **baremetal** project in the **MBED 6** version of *MBED-OS*.
	
When the type of project is selected, you can change the **project name**. Give a specific name corresponding to the content of the project.

.. figure:: ../_static/images/keil/keil_cloud_new_project_add.png
	:align: center
	:width: 70%

You can uncheck the :menuselection:`Initialize this project as a Git repository` option if you are not using Git with your project.

Click :menuselection:`Add project`. Your first project is created. 

.. figure:: ../_static/images/keil/keil_cloud_first_project.png
	:align: center
	
You can check in the :menuselection:`Libraries Manager` tab (in the bottom-right part of the interface) the version of MBED that it is used (in this example: MBED version 6.13).

|

Now it's time to test your first application, go to the :ref:`Compile and test <mbed_blinky>` section.


.. _mbed_studio_project:

MBED Studio
***********

.. note::

	In this section, we assume that you have a MBED account and that MBED Studio is installed on your computer. See :ref:`Keil Studio Cloud account <keil_studio_cloud>`.
	

Start :menuselection:`MBED Studio`.

MBED Studio IDE
===============

You will access to the main window of the :abbr:`IDE (Integrated Development Environment)`.

This interface is divided in a classical manner with a **project management** area (on the left side of the interface), a **text editor** area (in the top-right part of the interface) and an **output information** area (in the bottom-right part of the interface).

.. figure:: ../_static/images/keil/keil_mbed_studio_plus.png
	:align: center

	Main window of the MBED Studio software.
	

During your first access, no projects appear in the **project management** part. In this section, you can access to the list of the projects you develop (icon surrounded by a **pink** border).

Define your workspace
=====================

Before creating your first project, you need to specify where you want to store your projects.

Click :menuselection:`File -> Open Workspace...`. Then select the directory where you want to store your projects.

Create your first project
=========================

To create a new project, you can click :menuselection:`+ New Project` (icon surrounded by a **red** border on the previous figure) or click :menuselection:`File -> New Program`.

.. figure:: ../_static/images/keil/keil_mbed_studio_new_program.png
	:align: center
	:width: 70%

	:menuselection:`File -> New Program` in MBED Studio.

Then select :menuselection:`MBED6 -> mbed-os-example-blinky-baremetal`.

.. figure:: ../_static/images/keil/keil_mbed_studio_new_project_mbed_blinky.png
	:align: center
	:width: 70%
	
	New project selection. 
	
.. warning::

	To avoid any compilation conflicts with other libraries, make sure to select the **baremetal** project in the **MBED 6** version of *MBED-OS*.
	
When the type of project is selected, you can change the **project name**. Give a specific name corresponding to the content of the project.

.. figure:: ../_static/images/keil/keil_mbed_studio_new_project_add.png
	:align: center
	:width: 70%
	
	Add a new project in MBED Studio.


.. warning::

	In the **MBED OS Location** section, make sure to select the **Link to an existing shared Mbed OS instance** option, and select the directory where an instance of the last MBED-OS is installed.

	
.. note::
	
	On the LEnsE labwork computers, the last version of MBED-OS is installed in :file:`S:\\mbed-os` and :file:`C:\\mbed-os` .
	
Click :menuselection:`Add project`. Your first project is created. 

.. figure:: ../_static/images/keil/keil_mbed_studio_first_project.png
	:align: center
	
|

Now it's time to test your first application.

.. _mbed_blinky:

Compile and test
****************

MBED-OS primarily uses **C++** as the programming language for developing applications and firmware. 

.. note::
	
	If you are not familiar with the **C++ language**, tutorials are available at the following address: `C++ - Basics and Object-Oriented Programming  <https://iogs-lense-training.github.io/cpp-basics-oop/>`_.

.. note::

	Most of the following steps are the same in *Keil Studio Cloud* and *MBED Studio*. Otherwise, a note will specify the differences.

Main file
=========

On the left side of the interface, click on your project (here :menuselection:`01_First_Project` to display its contents.

.. figure:: ../_static/images/keil/keil_main.png
	:align: center
	
	First project contents.
	
Projects basically contain about ten files and directories. They are useful at various stages of the project realization.

But the **most essential** is the :file:`main.cpp` file. It contains the :code:`main()` function that serves as the entry point of the program. 

Click :menuselection:`main.cpp` file to open it on the top-right side of the interface.

*We will see later its content.*

Select a target
===============

Although the MBED-OS operating system is designed for a wide range of microcontrollers from the STM32 family, it is necessary to **specify** to the compiler for which **target** the program is being developed.

.. figure:: ../_static/images/keil/keil_target_select.png
	:align: center
	:width: 60%
	
	Target selection.

.. note::

	At LEnsE, we mainly use Nucleo-L476RG and Nucleo-G431KB boards.

If you don't select a target, the **compilation button is not enabled**. When you select a target, some options of the compilation process are automatically set up.

.. figure:: ../_static/images/keil/keil_target_no.png
	:align: center
	:width: 60%
	
	No compilation options if no target is selected.

Compile
=======

The C++ program is not understandable by the microcontroller. A **compilation step** is necessary to translate your code to native language of the microcontroller: a list of basic instructions.

.. figure:: ../_static/images/keil/keil_compile.png
	:align: center
	:width: 30%
	
	Compilation button (in blue).

Click on the **build button** (the blue one with a *hammer*) to compile your code. In the bottom-right side of the interface, the list of the files being compiled is display.

.. note::

	In the MBED Studio version, you can choose the *Build profile*. In *Debug* mode, you have access to inline debugging tools but it tooks more spaces in the memory contrary to the *Release* mode. 

After a few moment, and if no error occured during the compilation process, you obtain the same type of informations as displayed in the next figure:

.. figure:: ../_static/images/keil/keil_compile_output.png
	:align: center
	:width: 70%
	
	End of successful compilation process.

Depending on the development environment you used, you have two options.

Keil Studio Cloud
-----------------

A **binary file** is generated and downloaded on your computer (depending on your browser options).

.. figure:: ../_static/images/keil/keil_compile_bin_file.png
	:align: center
	:width: 40%

	Binary file to download.

MBED Studio
-----------

A binary file is created in a sub-directory of your project directory. Depending on the target you specified, the binary file is stored in the :file:`project_dir\\BUILD\\NUCLEO_target\\ARM6\\` directory, where *target* is the name of the target (for example: G431KB) and *project\_dir* the name of the directory where you stored your project.

.. figure:: ../_static/images/keil/keil_compile_file_dir.png
	:align: center
	:width: 80%

|

Flash the program
=================

The final step, before enjoying to play with your new system, is to **flash the binary file into the microcontroller**. *STMicroelectronics*, through the design of their Nucleo boards, facilitates the code uploading step into the microcontroller.

.. note::

	Make sure that your board is connected to your computer via a USB cable.

The Nucleo boards are recognized on computers as **USB storage devices**. But you can only store binary files as the previously generated by MBED compiler.

.. figure:: ../_static/images/nucleo/nucleo_usb_device.png
	:align: center
	:width: 40%

	G431KB Nucleo boards recognized as a USB storage device.


You just have to **copy and paste** the binary file (bin extension) from your computer to the Nucleo device. After few seconds, the Nucleo device flashes the internal memory of the onboard-microcontroller.

During the transfer of the file, the **LD1** (or **COM**) led is blinking in red and green. At the end of the transfer, this led stops blinking.

Duplicate a project
*******************

.. note::
	
	It is recommended to **create a new project** each time you develop a new application.
	
Instead of entirely creating a new project each time, you can also **duplicate an existing project**.

Right-click on the project you want to duplicate and click :menuselection:`Duplicate` .

.. figure:: ../_static/images/keil/keil_duplicate.png
	:align: center
	:width: 70%
	
A second project with the same name following by the term *copy* is generated. You can change its name by right-click on the new project and then click :menuselection:`Rename` . 

.. figure:: ../_static/images/keil/keil_duplicate_project.png
	:align: center
	:width: 70%
	
You can also set this new project as the active one by right-click on the project and then click :menuselection:`Set Active Project` . 

Pre-compiler informations
*************************



