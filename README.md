vtk2vtu
=======

pvpython script to convert vtk files (unstructured grid) to vtu files


=======

uses pvpython: http://www.paraview.org/
use it by typing: 
pvpython conversion.py [vtk-File 1] [vtk-File 2] ... [vtk-File n]
or: 
pvpython conversion.py *.vtk

there seems to be a memory leak in rhe VTK-Reader or -Writer, so the convertall script ist used to convert batches of 50 files and then restart pvpython to release the memory. This script removes the vtk-Files