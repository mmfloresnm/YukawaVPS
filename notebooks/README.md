# notebooks/

## Description

Contains Mathematica notebooks implementing the variable-phase method for computing scattering phase shifts and Sommerfeld factors, calculating quantities derived from the irregular solution, and evaluating scattering cross sections relevant to self-interacting dark matter.

* `YukawaVPS.nb`: Main notebook for computing partial-wave phase shifts, Sommerfeld factors, and quantities derived from the irregular solution, including the function $T(k,k_\diamond)$ used in the treatment of inelastic scattering. Includes routines for parameter scans over the dimensionless variables $\xi$ and $\zeta$ at fixed angular momentum $\ell$, as well as utilities for importing and interpolating the provided precomputed data.

* `CrossSectionsVPS.nb`: Notebook for computing differential, elastic, transfer, and viscosity cross sections from the phase shifts. Includes routines for evaluating cross sections over the parameter grid, determining the partial-wave truncation required for convergence, and importing, exporting, and interpolating cross-section data.
