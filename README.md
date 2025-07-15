# Dynamic source inversion input files
This repository contains all input files that are required to run the dynamic source inversion with FD3D_TSN ([Premus et al., 2020](https://doi.org/10.1785/0220190374)). The listed input files are exemplarly for the 2004 Parkfield, California earthquake ([Schliwa et al., 2024](https://doi.org/10.1029/2024JB029410)). 

# Code input parameter files
`input.dat` contains general input parameters as the fault geometry, the number of Green's function sources, and the number of seismic and GPS receivers.

`inputfd3d.dat` provides the numerical discretization for the finite-difference dynamic rupture solver.

`inputgps.dat` contains the postseismic modeling duration, the number of GPS receivers, and their weights. 

`ìnputinv.dat` describes the inversion settings, including the model parameter discretization, their range, and their step size. The number in the first line dictates whether the code runs a single forward calculation `0`, starts an inversion `1`, or restarts an inversion `2`.
