Execution time
##############



Some examples
=============

In this section, we assume that variables a, b, and c are of type integers, and variables x, y and z are of type double.

.. list-table:: Comparison of execution time of various calculations across different platforms.
   :widths: 25 25 25 25
   :header-rows: 1

   * - Instruction
     - C++ CPU
     - L476RG
     - G431KB
   * - no operation
     - /
     - 
     - ~26 ns
   * - out_pin = 1;
     - /
     - 
     - ~22 ns
   * - c = a + b;
     - 
     - 
     - < 50 ns
   * - c = a * a;
     - 
     - 
     - < 50 ns
   * - c = pow(a, 2);
     - 
     - 
     - ~6.5 us
   * - z = x + y;
     - 
     - 
     - 