# Dynamic source inversion input files
This repository contains all input files that are required to run the dynamic source inversion with FD3D_TSN ([Premus et al., 2020](https://doi.org/10.1785/0220190374)). The listed input files are exemplary for the 2004 Parkfield, California earthquake ([Schliwa et al., 2024](https://doi.org/10.1029/2024JB029410)). 

## Code input parameter files
`input.dat` contains general input parameters as the fault geometry, the number of Green's function sources, and the number of seismic and GPS receivers.

`inputfd3d.dat` provides the numerical discretization for the finite-difference dynamic rupture solver.

`inputgps.dat` contains the postseismic modeling duration, the number of GPS receivers, and their weights. 

`ìnputinv.dat` describes the inversion settings, including the model parameter discretization, their range, and their step size. The number in the first line dictates whether the code runs a single forward calculation `0`, starts an inversion `1`, or restarts an inversion `2`.

`forwardmodel.dat` contains the dynamic friction and prestress parameters across the defined fault plane. This represents the starting model when running an inversion.

## Material properties and receiver information

`crustal.dat` provides the 1D material structure.

`stations.dat` and `stations_GPS.dat` provide the local model coordinates of the seismic and GPS stations.

`stainfo.dat` and `gpsinfo.dat` set which components of a receiver are computed and how they are weighted.

`stations.in` provides the latitude and longitude of the epicenter, which was used to calculate the local model coordinates.

## Seismic and geodetic observations

`rvseis*.dat` contain the different components of seismic observations, which constrain the dynamic source inversion

`rvgpsnez.dat` contains coseismic and three months of postseismic GPS observations

## Green's functions 

`sources.dat` provides the locations across the fault plane, for which Green's functions have been calculated.

`NEZsorGPS.dat` contains the Green's functions for the GPS receivers.



