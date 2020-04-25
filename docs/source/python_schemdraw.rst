
SchemDraw
=========

https://schemdraw.readthedocs.io/en/latest/usage/placement.html



.. code:: python

   import SchemDraw

   d = SchemDraw.Drawing()



Gate
----

https://schemdraw.readthedocs.io/en/latest/elements/logic.html


Typical AND, OR, NAND, NOR, XOR, XNOR, and NOT gates with 2, 3, or 4 inputs are predefined.

Anchors are defined as ‘in1’, ‘in2’, etc. for each input, and ‘out’ for the output.


.. code:: python

   import SchemDraw
   from SchemDraw import logic