# szabo-f2py
The book "Modern Quantum Chemistry" by Szabo and Ostlund includes example Fortran code to perform a simple Hartree-Fock calcuation on HeH+.
The example code, [szabo.f](http://www.ccl.net/cca/software/SOURCES/FORTRAN/szabo/index.html), is available on ccl.net.  

The plan for this repository is to create an f2py wrapper for the example so that it can be called from python.
The python wrapper will be used to write unit tests for the example.

## Building

Use f2py3 to generate a wrapper for szabo.f.
```
f2py3 -c szabo-f2py/src/szabo.f -m hfcalc
```
This while compile the Python extension with the name hfcalc, which is the subroutine in szabo.f that implements the calculation.
The driver code has been commented out and moved to the Python file szabo.py.

## See Also
* [szabo.py](https://github.com/lcb/szabo.py) - Python re-implementation of szabo.f
