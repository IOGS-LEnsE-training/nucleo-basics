Digital inputs and outputs
##########################

Digital signals
***************

Binary Digits
=============

A **digital signal** is a type of signal that represents data as **discrete values**, using **binary digits** (*bits*). 

In digital signals, the information is encoded as a sequence of binary numbers, where **each bit** can have one of **two possible states**: '0' or '1'.

Digital signals are the **primitive signals** of microcontrollers. All the internal data transit as '0' or '1' between the different main organs: memories, processing units...

Digital carrier signals
=======================

In digital systems, bits are typically carried using **electronic signals**. These signals can be represented by different physical phenomena such as **voltage levels** in electrical circuits, **light pulses** in optical fibers, or magnetic polarities in magnetic storage devices.

In STM32 microcontrollers on Nucleo boards, two different voltage levels are used:

* 0V for logical '0'
* 3.3V for logical '1'


Digital Ouputs
**************

Digital outputs are often used in microcontroller-based systems for **interfacing with the external world**.

They are commonly used in electronic systems **to control devices** such as motors, lights, or relays, where the output state determines whether the device is on or off, open or closed, etc. 

Declare an output
=================

Digital ouput are described by the :class:`DigitalOut` class from the *mbed.h* library.

.. code-block:: C++

	DigitalOut var_name(PIN_NAME);
	
As a bridge with the external world, this instruction required a valid *PIN_NAME*.

Update an output
================



Digital Inputs
**************

.. warning::

	Voltage between 0 and 3.3V !
	