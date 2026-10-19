# YukawaPhaseAndSommerfeld
This repository accompanies [PAPER CITATION] and provides the Mathematica implementation and precomputed data for numerical calculations of scattering in a Yukawa potential.

The repository includes routines for computing partial-wave phase shifts and Sommerfeld factors using the variable-phase method, quantities derived from the irregular solution for applications involving inelastic scattering, and elastic, transfer, and viscosity cross sections relevant to self-interacting dark matter.

## Repository contents
* `notebooks/`: Mathematica notebooks implementing the numerical calculations.
* `data/`: Precomputed phase shifts, Sommerfeld factors, irregular-solution quantities, and scattering cross sections.

For a description of the numerical implementation, notebook examples, data format, and instructions for importing and interpolating the tabulated results, see the [User Guide](./user_guide.pdf).

## Requirements

The numerical calculations are implemented in Mathematica. The `MaTeX` package is used for plotting and is recommended for reproducing the included plotting examples. See the [MaTeX repository](https://github.com/szhorvat/MaTeX) for installation instructions. The precomputed datasets are provided as plain-text files that can be used independently of Mathematica.

## Attribution

If you use the code or data in this repository in your research, please cite the accompanying paper:

[FULL PAPER CITATION]

For details of the numerical method and its theoretical basis, please also cite the relevant references given in the paper.

## License

See LICENSE for the terms under which this repository's code and data may be used.