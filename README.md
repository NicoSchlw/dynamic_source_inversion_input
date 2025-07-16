# Dynamic Source Inversion Input Files

This repository contains all necessary input files to perform a dynamic source inversion using **FD3D_TSN** ([Premus et al., 2020](https://doi.org/10.1785/0220190374)). The included files are exemplary for the 2004 Parkfield, California earthquake ([Schliwa et al., 2024](https://doi.org/10.1029/2024JB029410)).

---

## Input Parameter Files

- **`input.dat`**  
  Defines general model parameters including fault geometry, the number of Green's function sources, and the number of seismic and GPS receivers.

- **`inputfd3d.dat`**  
  Specifies numerical discretization parameters for the finite-difference dynamic rupture solver.

- **`inputgps.dat`**  
  Sets the postseismic modeling duration, number of GPS receivers, and their respective weights.

- **`inputinv.dat`**  
  Describes inversion settings including model parameter discretization, parameter ranges, and step sizes. The first line determines the mode:  
  - `0`: Single forward simulation  
  - `1`: Start a new inversion  
  - `2`: Restart a previous inversion

- **`forwardmodel.dat`**  
  Contains the initial model of dynamic friction and prestress parameters across the fault plane, used as the starting point for inversion.

---

## Material Properties & Receiver Information

- **`crustal.dat`**  
  Specifies the 1D crustal velocity and density structure.

- **`stations.dat`** and **`stations_GPS.dat`**  
  Define the local model coordinates of seismic and GPS stations, respectively.

- **`stainfo.dat`** and **`gpsinfo.dat`**  
  Configure which receiver components are used and how they are weighted during inversion.

- **`stations.in`**  
  Provides the epicenter's latitude and longitude used to derive local model coordinates.

---

## Seismic and Geodetic Observations

- **`rvseis*.dat`**  
  Files containing different components of seismic observations used to constrain the dynamic source inversion.

- **`rvgpsnez.dat`**  
  Contains both coseismic and three months of postseismic GPS data.

---

## Green’s Functions

- **`sources.dat`**  
  Lists the locations on the fault plane where Green's functions were computed.

- **`NEZsorGPS.dat`**  
  Provides Green's functions corresponding to the GPS receiver locations.

---
