MBED Compiler and Keil Studio IDE
#################################

Programming languages for microcontrollers 
******************************************

Microcontrollers (UCs) typically have **specific constraints and architectures** that developers must consider when designing software for them:

#. Memory Constraints and Code Size
#. Processing Power
#. Peripheral Limitations, but high level of responsiveness to external demands

Understanding and addressing these constraints is essential for designing robust, efficient, and reliable software for microcontroller-based systems. It requires careful consideration of hardware limitations, application requirements, and software design principles throughout the development process.


Assembly language
=================

Assembly language is commonly used for programming microcontrollers due to **its low-level nature** and direct control over hardware resources. When programming microcontrollers in assembly language, developers write **instructions that directly correspond to the machine-level operations** executed by the microcontroller's processor. This level of control can be beneficial for applications requiring precise timing, minimal resource usage, or interaction with specific hardware features.

While programming microcontrollers in assembly language provides maximum control and efficiency, it **comes with challenges** such as complexity, longer development time, and reduced portability compared to higher-level languages like C or C++.

C++ language
============

C++ is increasingly being used for microcontroller programming, especially with microcontrollers that have more **powerful processors** and sufficient memory resources. Here are some key points about using C++ for microcontroller development:

#. **Object-Oriented Programming (OOP)**: C++ is an object-oriented programming language, allowing developers to use concepts like classes, inheritance, encapsulation, and polymorphism. This can lead to **more modular** and maintainable code, which is advantageous for larger projects.

#. **Standard Template Library (STL)**: C++ includes a rich standard library, including containers (like vectors, arrays, and maps), algorithms, and utilities. Although the standard library may not always be suitable for resource-constrained microcontrollers, parts of it can still be utilized depending on the microcontroller's capabilities.
#. **Portability**: C++ code written for microcontrollers can be highly portable across different platforms, provided that the code doesn't rely on platform-specific features or hardware-dependent optimizations.
#. **Toolchain Support**: Many modern microcontroller development toolchains, including compilers and IDEs, provide support for C++ development. This includes popular microcontroller families such as ARM® Cortex-M® series, AVR, PIC, and others.

.. caution::
	
	When using C++ for microcontroller development, it's essential to be mindful of the **specific constraints and characteristics** of the target microcontroller, including its memory resources, processing power, and available peripherals. 

C++ is not a low-level language that can be understood by a microcontroller core. Using C++ language requires a compiler, that translates this high-level language to the native language of the microcontroller (assembly instructions).


MBED free open source IoT operating system
******************************************

Mbed is an **open-source embedded operating system** designed by Arm®, a leading semiconductor and software design company, for microcontroller-based applications. It provides a platform and ecosystem for rapid prototyping, development, and deployment of embedded systems. 

It includes **Mbed OS**, a lightweight, **open-source operating system** specifically designed for microcontrollers. It abstracts away low-level hardware details and provides a consistent API for accessing peripherals.

It also provides a comprehensive set of development tools, including a free Integrated Development Environment (IDE) called the **Mbed Studio**.

Mbed has a vibrant community of developers, contributors, and partners who contribute libraries, example codes, and resources to the ecosystem. This rich ecosystem makes it easier for developers to find support, collaborate, and leverage existing components for their projects. 

The **LEnsE** team also develops **ressources** (libraries and examples) for Mbed-OS: `MBED6 Libraries <https://iogs-lense-ressources.github.io/mbed6-libraries/>`_.


.. warning::

	At the moment **Mbed Studio** supports **only Mbed login** (created on https://os.mbed.com/).
	
	**Keil Studio Cloud** supports both Mbed and Arm® accounts


.. _keil_studio_cloud:

Keil Studio Cloud
*****************

The Keil division of Arm® provides a **web-based platform** for embedded software development, particularly for STM32 microcontroller-based projects, called **Keil Studio Cloud**

This online version integrates various tools necessary for embedded development, including code editing, compiling, debugging, and project management, all within a web browser interface.

You can access to this platform by following this link: https://www.keil.arm.com/. 

.. figure:: ../_static/images/keil/keil_website.png
	:align: center	

To manage project under this web-based tool, you need to **create an account** on the Keil website. Click :menuselection:`Keil Studio Cloud`.

.. figure:: ../_static/images/keil/keil_signup.png
	:width: 60%
	:align: center

Then :menuselection:`Sign Up`.

Follow the different steps until your account is validated. 

.. note::

	The validation of your email address may take a few minutes.

.. figure:: ../_static/images/keil/keil_cloud.png
	:width: 80%
	:align: center

	Interface of Keil Studio Cloud.


MBED Studio
***********

A client (or local) version, called **Mbed Studio** and developed by Arm® is also available.

.. warning::

	At the moment **Mbed Studio** supports **only Mbed login** (created on https://os.mbed.com/).

It provides a comprehensive set of tools for developing, compiling, debugging, and deploying firmware for microcontroller-based devices. It offers the same features as Keil Studio Cloud, except that it required to be locally installed on your computer. 

You can download the last version on the Mbed web site: https://os.mbed.com/studio/.

.. figure:: ../_static/images/keil/keil_mbed_studio.png
	:width: 80%
	:align: center

	Interface of MBED Studio.

At first use, you must be connected to the Internet and have a Mbed account. But after the first use, no internet connection is required.

