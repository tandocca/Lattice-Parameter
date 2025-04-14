# Lattice-Parameter

This repository contains relevant code and data for "A bond-based model for accurate prediction of lattice parameter of bcc solid solution alloys" by Christopher Tandoc, Liang Qi, and Yong-Jie Hu. Liaw to be published in Materialia

LP_tool.py is a linux command line script written in python that takes a chemical composition in the form of a text string and prints the lattice parameter in angstroms.

example usgage: ./LP_Tool.py Ti0.5V0.5

The tool can also be implemented into your own code such as shown in the example below:

import LP_Tool

LP = LP_Tool.get_LP("Ti0.5V0.5")

-This script uses pymatgen (https://pymatgen.org/) to process the input string and is thus a requirement for the script to work. Depending on the version of pymatgen you have installed, lines 3 and 380 may need to be modified (https://matsci.org/t/python-problem-with-pymatgen/35720)

-This tool is currently only able to make predictions for compositions containing Al,Ti,Zr,Hf,V,Nb,Ta,Cr,Mo,W,Re,Ru and will return an error if any other elements are present in the input 

-B2 and elemental bond lengths are defined in dictionaries at the beginning of the code
