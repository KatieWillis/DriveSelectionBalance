# DriveSelectionBalance

___
This repository contains jupyter and mathematica notebooks associated with the manuscript "Engineering drive-selection balance for localised population suppression with neutral dynamics" currently available on BioRXiv. The notebooks and associated files contain all code needed to reproduce all analysis, figures and tables included in the manuscript. 

Katie Willis1 & Austin Burt1

1 Department of Life Sciences, Imperial College London, London, UK.


For correspondence regarding the code: katie.willis@imperial.ac.uk

___
## Requirements

* Julia 1.9 or above
* Jupyter notebook
* This analysis was performed on macOS Sonoma 14.3, however any system which can run Julia 1.9 should be suitable.  
* All dependencies can be installed by running the following code in julia from the location of the downloaded files to initiate the environment (This only needs to be done once)
```
using Pkg
Pkg.activate("./Environment/")
Pkg.instantiate()
```

The environment can loaded at the beginning of each jupyter session by running:
```
] activate "./Environment/"
```

And the required packages can be loaded by running:
```
using NBInclude
@nbinclude("./Environment/Setup.ipynb");
```

Alternatively the packages can be installed manually:
```
CSV v0.10.12
DataFrames v1.6.1
DelimitedFiles v1.9.1
JLD2 v0.4.45
NBInclude v2.3.0
Plots v1.39.0
PyPlot v2.11.2
SymPy v2.0.1
Tables v1.11.1
Distributed
LinearAlgebra
```

Installation is not expected to take more than 30 minutes
___
## User notes

- The AnalyticalModel.nb is a mathematica file containing the code used to analyse the single-locus, single-sex PDNE model. 
- The SimulatorScript.ipynb is a jupyter notebook which contains the code used to generate the figures and values associated with modelling more complex scenarios including two sexes, population dynamics and multiple loci.
- For each model a folder contain human readable .csv files with gamete tables and fitness costs associated with each genotype which are used alongside the functions within SimulatorFunctions.ipynb to run the simulations. 

___

## Timing:

Results requiring only a few time series simulations take only a few seconds. Results requiring more simulations, such as parameter sweeps or calucating release rate requirements, can take several minutes. 
___
