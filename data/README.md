# Data

The tabulated data (~6 GB) are distributed separately from this repository.

**Download:** [to be added]

Unpack the archives into this folder, so that it contains:

data/
├── zetaVSxi_grid.txt
├── AttractiveYukawa/
│   ├── PhaseShift/      PhaseShift_A_l=000.txt … PhaseShift_A_l=100.txt
│   ├── Sommerfeld/      Sommerfeld_A_l=000.txt … Sommerfeld_A_l=100.txt
│   ├── CrossSections/   sigelas_A.txt, sigT_A.txt, sigV_A.txt
│   ├── lmax/            lmax_elas_A.txt, lmax_T_A.txt, lmax_V_A.txt
│   └── T/               T_A_l=000.txt
└── RepulsiveYukawa/
    └── (same as above with A → R; no T/ directory)

The notebooks look for the data in `../data/` by default (relative to the
notebook folder). A different location can be set with the
`"OutputDirectory"` option of the import functions.

## Contents

- Grid: log10|ζ| ∈ [−4, 7], log10 ξ ∈ [−6, 5], step 0.01, excluding 10|ζ| < ξ.
- Phase shifts θ_ℓ ∈ (−π, π] and Sommerfeld factors S_ℓ for ℓ = 0, …, 100.
- Elastic, transfer, and viscosity cross sections normalized to 4π/k²
  (distinguishable particles), with partial waves up to ℓ = 100, 99, 98.
- ℓ_max: smallest ℓ beyond which the estimated relative truncation error
  stays below 1%.
- T(k; k⋄) for ζ⋄ = 1, s-wave, attractive potential only.

## Format

`zetaVSxi_grid.txt` lists the full (ξ, |ζ|) grid, one point per row, with |ζ|
running fastest. All other files contain a single column of values in the
same order, **only** for points with ξ ≤ 10|ζ|. Use `importGrid` and the
import functions in the notebooks to map the data onto the grid.

See `user_guide.pdf` for details and the paper for definitions.