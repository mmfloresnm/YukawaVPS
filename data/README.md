# data/

## Download

The data (~6 GB) are archived on Zenodo: [doi:10.5281/zenodo.23475703](https://doi.org/10.5281/zenodo.23475703).

1. Download `data.zip` and place it in the repository root (the folder containing `user_guide.pdf`).
2. From the repository root, run:

```bash
   unzip data.zip
```

This adds `zetaVSxi_grid.txt`, `AttractiveYukawa/`, and `RepulsiveYukawa/` to this directory. This README is left unchanged.

Use the command line rather than double-clicking. Graphical tools such as Finder or Windows "Extract All" may create a separate folder (e.g., `data 2/` or `data/data/`) instead of merging into this one.

After unzipping, the directory should contain:

```
data/
├── README.md
├── zetaVSxi_grid.txt
├── AttractiveYukawa/
└── RepulsiveYukawa/
```

## Description

This directory contains precomputed data for scattering in the attractive and repulsive Yukawa potentials. The phase shifts, Sommerfeld factors, and irregular-solution quantities are computed using `YukawaVPS.nb`. The elastic, transfer, and viscosity cross sections, together with the corresponding partial-wave truncation values $\ell_{\max}$, are computed using `CrossSectionsVPS.nb`.

The datasets are provided to facilitate the use of these quantities without requiring the numerical calculations to be repeated. For details on the data format, import routines, and interpolation, see the [User Guide](../user_guide.pdf).

## Grid specification

All data are tabulated over the following parameter ranges:

* $\log_{10}|\zeta|\in [-4,7]$
* $\log_{10}\xi \in [-6,5]$, excluding points satisfying $10\, |\zeta| < \xi$
* Partial-wave index $\ell=0,\ldots,100$

The logarithmic grid spacing is $\Delta\log_{10}\xi=\Delta\log_{10}|\zeta|= 10^{-2}.$

Thus, $\xi$ and $|\zeta|$ are sampled uniformly in their base-10 logarithms, while $\ell$ takes integer values from 0 to 100.

The region $10\, |\zeta|<\xi$, which approaches the Coulomb limit, is excluded from the numerical scan. The parameter grid file includes this region, but the corresponding entries are omitted from the tabulated calculation results.

## Directory structure

The data are organized by potential type and observable:

* `PhaseShift/`: Partial-wave phase shifts $\theta_\ell(k)$.
* `Sommerfeld/`: Sommerfeld factors $S_\ell(k)$.
* `CrossSections/`: Elastic, transfer, and viscosity cross sections, normalized to the $s$-wave unitarity cross section $\sigma_{\ell=0}^{\mathrm{U}}=4\pi/k^2$.
* `lmax/`: Smallest $\ell_{\max}$ beyond which the geometric-tail estimate of the relative truncation error remains below 1%.
* `T/`: Irregular-solution data $T(k;k_\diamond)$, provided for the attractive potential and the $s$-wave only.

The data are stored in `AttractiveYukawa/` and `RepulsiveYukawa/`, with files labeled `A` and `R`, respectively. The `T/` directory is present only for the attractive potential.

The file `zetaVSxi_grid.txt` contains the parameter grid. Note that the grid includes points in the excluded region, whereas the corresponding observable files contain entries only for points included in the numerical calculations. See the [User Guide](../user_guide.pdf) for details on mapping the data to the grid and using the provided import and interpolation routines.

## License

The data are distributed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).