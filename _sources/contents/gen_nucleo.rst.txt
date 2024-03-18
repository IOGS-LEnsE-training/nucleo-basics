Nucleo boards and STM32 MCU
###########################


Rapid prototyping boards
************************

Nucleo boards are a series of **development boards** designed by `STMicroelectronics <https://www.st.com/content/st_com/en.html>`_. They are specifically tailored for **rapid prototyping** and **easy development** of microcontroller-based projects.

Nucleo boards typically feature an **STM32** microcontroller unit (MCU) as their core component, which belongs to the ARM® Cortex-M® family. 

.. figure:: ../_static/images/nucleo/nucleo_boards.png
	:align: center
	:width: 70%

	Nucleo-G431KB (left) and Nucleo-L476RG (right) boards.

These boards offer a variety of features such as on-board debugging and programming interfaces, multiple :abbr:`GPIO (General Purpose Input/Output` pins, integrated sensors, connectivity options, as well as expansion headers for **connecting additional hardware modules**.

There are different formats of Nucleo boards: in the previous figure, you can see a small-size Nucleo-32 board on the left (i.e. 32 available pins) and a middle-size Nucleo-64 on the right (i.e. 64 available pins).

Nucleo boards are popular among hobbyists, students, and professional developers due to their affordability, versatility, and ease of use. Different **integrated development environment (IDE)** support could be used to develop program for **STM32** MCU: 

* `STM32CubeMX / STM32CubeIDE <https://www.st.com/en/ecosystems/stm32cube.html>`_
* Keil µVision
* `MBED Studio <https://os.mbed.com/studio/>`_ / `Keil Studio Cloud <https://www.keil.arm.com/>`_


Nucleo boards serve as a **convenient platform** for learning embedded systems programming, experimenting with various sensors and peripherals, and prototyping IoT (Internet of Things) applications.



Pins and their functions
########################

Each pin of the boards can have multiple functions. But only one can be used at a time.

.. figure:: ../_static/images/nucleo/nucleo_pin_functions.png
	:align: center

	Example of a Nucleo pin.

In the previous example, the **PA_7** pin (name given by *STMicroelectronics*) can be used as:

* a **digital input or output** (true for lot of pins of STM32 microcontrollers)
* an **analog input**, linked to an :abbr:`ADC (Analog-to-Digital Converter)` , as indicated by the :menuselection:`AnalogIn` tag
* a **pulsed-width modulated output**, as indicated by the :menuselection:`PWM` tag
* another specialized function pin (:abbr:`MOSI (Master Out Slave In)` pin of a :abbr:`SPI (Serial Peripheral Interface)` communication in this case)

Other options are possible, such as:

* **analog output**, linked to a :abbr:`DAC (Digital-to-Analog Converter)` , indicated by an :menuselection:`AnalogOut` tag
* :abbr:`UART (Universal Asynchronous Receiver/Transmitter)` or :abbr:`USART (Universal Synchronous/Asynchronous Receiver/Transmitter)` communication pins, indicated by a :menuselection:`Serial` tag
* :abbr:`I2C (Inter-Integrated Circuit)` communication pins, indicated by an :menuselection:`I2C` tag
* :abbr:`SPI (Serial Peripheral Interface)` communication pins, indicated by a :menuselection:`SPI` tag

Pin indicated with a :menuselection:`GND` tag correspond to the ground voltage, i.e. the 0V reference voltage of the board.

Some other pins are not directly linked to the microcontroller, but give access to regulated power supply: such as **3.3V** or **5V**.

.. warning::

	Regulated voltage outputs are current-limited. See the documentation of the Nucleo board you are using.
	
A power supply input can be used to power the board. It is tagged as :menuselection:`Vin`.

.. warning::

	The input **Vin** voltage must be between 7 and 12 volts.

.. _nucleo_g431kb_pinouts:

G431KB board - Nucleo-32
************************

PICTURE OF PINOUT

.. _nucleo_l476rg_pinouts:

L476RG board - Nucleo-64
************************

Download :download:`Nucleo-64_L476RG <../_static/docs/Nucleo-64_L476RG.pdf>`

Morpho connectors
=================

.. figure:: ../_static/images/nucleo/l476rg/l476rg_CN7.png
	:align: center
	
.. figure:: ../_static/images/nucleo/l476rg/l476rg_CN10.png
	:align: center	

Arduino connectors
==================

.. figure:: ../_static/images/nucleo/l476rg/l476rg_CN8.png
	:align: center
	
.. figure:: ../_static/images/nucleo/l476rg/l476rg_CN5.png
	:align: center	

.. _nucleo_f767zi_pinouts:

F767ZI board - Nucleo-144
*************************

PICTURE OF PINOUT
