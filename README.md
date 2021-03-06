**RI Calculator**

This program allows to apply the RI methodology developed by Esnouf, A et al. (see reference below) within the Life Cycle Assessment methodology (LCA).
RIs are indexes of the relevance of Life Cycle Impact Assessment methods (LCIA) or impact categories to study one or several system Life Cycle Inventories (or aggregated LCIs) in the global context of their database. This first version of the program is only compatible with simapro exports and LCIs modeled with ecoinvent 3.1 database version “allocation at the point of substitution”.
The version of the analyzed LCIA methods can be found in *methods.txt*. LCIA methods are provided with the Simapro nomenclature. The standardization of LCIA method has already been applied.

RIs for a LCIA method and for each of its impact categories can be obtained.
RIs from orthogonalized impact categories are also calculated to avoid over/underrepresentation of LCI when several impact categories are correlated.

**Usage**

*RI_Calculator.py* is the main script where directories and excel LCI names have to be specified by the user . 
Running this script will use the different python modules supplied in the package. Needed external python packages are listed in requirements.txt.

The generated RIs results are stored as excel file in the second specified directory.

**Implementation**

Using *lci_formatting.py*, LCIs are formatted (to modify their format from the simapro export format) and standardized with the geometric means of the ecoinvent 3.1 dimensions.
The impact category RIs are then determined (*ri_calculation.py*).

To obtain the LCIA method RIs, methods have to be formatted to organize and orthogonalize them (*method_formatting.py*).
Then, RIs of LCIA methods are determined (*ri_calculation.py*).

**Reference:**
Esnouf, A et al. _Representativeness of environmental impact assessmentmethods regarding Life Cycle Inventories_,
Sci Total Environ (2017), https://doi.org/10.1016/j.scitotenv.2017.10.102

_This project is licensed under the terms of the MIT license._