# YukawaVPS
This repository accompanies [PAPER CITATION] and provides the Mathematica implementation of numerical calculations of scattering in a Yukawa potential, together with precomputed data archived on Zenodo.

The repository includes routines for computing partial-wave phase shifts and Sommerfeld factors using the variable-phase method, quantities derived from the irregular solution for applications involving inelastic scattering, and elastic, transfer, and viscosity cross sections relevant to self-interacting dark matter.

## Repository contents
* `notebooks/`: Mathematica notebooks implementing the numerical calculations.
* `data/`: Location for the precomputed phase shifts, Sommerfeld factors, irregular-solution quantities, and scattering cross sections. The data (~6 GB) are archived on Zenodo ([doi:10.5281/zenodo.23475703](https://doi.org/10.5281/zenodo.23475703)); see [`data/README.md`](./data/README.md) for download and setup instructions.

For a description of the numerical implementation, notebook examples, data format, and instructions for importing and interpolating the tabulated results, see the [User Guide](./user_guide.pdf).

## Requirements

The numerical calculations are implemented in Mathematica. The `MaTeX` package is used for plotting and is recommended for reproducing the included plotting examples. See the [MaTeX repository](https://github.com/szhorvat/MaTeX) for installation instructions. The precomputed datasets are provided as plain-text files that can be used independently of Mathematica.

## Attribution

If you use the code or data in this repository in your research, please cite the accompanying paper:

[FULL PAPER CITATION]

If you use the tabulated data, please also cite the dataset:

M. M. Flores, K. Petraki, and T. Pignard, *YukawaVPS data: phase shifts, Sommerfeld factors, and cross sections for Yukawa scattering*, Zenodo (2026), [doi:10.5281/zenodo.23475703](https://doi.org/10.5281/zenodo.23475703).

For details of the numerical method and its theoretical basis, please also cite the relevant references given in the paper.

## License

The code and documentation in this repository are distributed under the MIT License (see [LICENSE](./LICENSE)). The tabulated data, archived on Zenodo ([doi:10.5281/zenodo.23475703](https://doi.org/10.5281/zenodo.23475703)), are distributed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).