# Protein Structure Comparison using c-RMSD and d-RMSD

This repository contains a easy to use script for comparing two protein structures — the SARS-CoV-2 main protease in complex with an inhibitor (PDB ID: 6LU7) and the SARS-CoV main protease (PDB ID: 2AMD) — using two structural similarity metrics:

- **c-RMSD (Cartesian Root Mean Square Deviation)**: based on direct atom-to-atom distances.
- **d-RMSD (Distance-based RMSD)**: based on comparison of all intra-molecular distances.

we show how to extract alpha carbon (Cα) coordinates from `.pdb` files, align structures using UCSF ChimeraX, and compute both c-RMSD and different versions of d-RMSD in Python.

---

## Files

- `struct1.ipynb`: Jupyter notebook containing the RMSD calculations.


> Note: You can align structures using UCSF ChimeraX and export the aligned models as PDB files to use with this notebook.

---

## How to Use

Simply open the notebook and run it. It will:
- Parse the aligned `.pdb` files
- Extract Cα atom coordinates
- Compute:
  - c-RMSD between matched atoms
  - d-RMSD using:
    - all Cα–Cα pairs
    - the 600 shortest distance pairs
    - 600 random distance pairs

All methods are implemented in plain Python using `Bio.PDB` and `NumPy`.

---

## Citations

- **Protein Structures** from the RCSB Protein Data Bank:  
  Berman, H.M., et al. (2000) *The Protein Data Bank*. Nucleic Acids Research, 28, 235–242. https://doi.org/10.1093/nar/28.1.235

- **ChimeraX** for structure alignment and visualization:  
  Pettersen, E.F., et al. (2021) *UCSF ChimeraX: Structure visualization for researchers, educators, and developers*. Protein Science, 30(1), 70–82. https://doi.org/10.1002/pro.3943

- **Biopython** used for parsing PDB files:  
  Cock, P.J.A., et al. (2009) *Biopython: freely available Python tools for computational molecular biology and bioinformatics*. Bioinformatics, 25(11), 1422–1423. https://doi.org/10.1093/bioinformatics/btp163

- **NumPy** for scientific computing:  
  Harris, C.R., et al. (2020) *Array programming with NumPy*. Nature, 585, 357–362. https://doi.org/10.1038/s41586-020-2649-2

---

## License

This project is licensed under the MIT License. Feel free to reuse or adapt the code.

---

## Keywords

c-RMSD, d-RMSD, protein structure, RMSD tutorial, PDB file, UCSF ChimeraX, structural alignment, C-alpha, bioinformatics, structural biology, python
