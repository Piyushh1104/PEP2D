# PEP2D: Peptide Secondary Structure Prediction using Evolutionary Information

## Overview

PEP2D is a computational method developed specifically for predicting the secondary structure of peptides using evolutionary information and machine learning approaches.

The platform was designed because existing protein secondary structure prediction methods perform poorly on short peptides. PEP2D predicts peptide secondary structures into three major classes:

- Helix (H)
- Beta-sheet (E)
- Coil (C)

The method uses:

- Binary profile features
- Evolutionary information (PSSM profiles)
- Random Forest
- IBK
- Artificial Neural Networks (ANN)

Web Server:

https://webs.iiitd.edu.in/raghava/pep2d/

---

## Research Paper

**Title:** Peptide Secondary Structure Prediction using Evolutionary Information

**Authors:**  
Harinder Singh, Sandeep Singh and Gajendra Pal Singh Raghava

**Publication Type:** bioRxiv Preprint (2019)

**Correct DOI:**  
https://doi.org/10.1101/558791



---

## Background

Peptides are emerging therapeutic molecules because of:

- High specificity
- Low toxicity
- Easy synthesis
- Better tissue penetration
- Lower production cost

Secondary structure prediction is important for:

- Peptide therapeutics
- Drug discovery
- Structural bioinformatics
- Peptide engineering
- Bioactive peptide analysis

Existing secondary structure prediction methods were mainly designed for proteins, not peptides.

---

## Dataset Information

### PEP2D Dataset

The dataset was collected from Protein Data Bank (PDB).

Initial dataset:

- 5778 peptide chains

Final dataset:

- 3107 unique peptides
- Length range: 5–50 amino acids

Source: :contentReference[oaicite:1]{index=1}

---

## Dataset Subsets

| Dataset | Length Range | Number of Peptides |
|----------|--------------|-------------------|
| PEP2D5N10 | 5–10 | 572 |
| PEP2D11N20 | 11–20 | 718 |
| PEP2D21N30 | 21–30 | 610 |
| PEP2D31N50 | 31–50 | 1207 |

---

## Secondary Structure Assignment

Secondary structures were assigned using DSSP.

The eight DSSP states were grouped into:

| DSSP States | Final State |
|-------------|-------------|
| H, I, G | Helix (H) |
| B, E | Sheet (E) |
| S, T, C | Coil (C) |



---

## Input Features

### Binary Profile

Each residue was represented using a 20-dimensional binary vector.

### PSSM Profile

Evolutionary information was generated using:

- HHblits
- Multiple sequence alignment

PSSM profiles improved prediction accuracy significantly.

---

## Machine Learning Algorithms

The following algorithms were implemented:

- Random Forest
- IBK (Nearest Neighbor)
- Artificial Neural Networks (ANN)

Random Forest models showed the best overall performance.

Source: :contentReference[oaicite:3]{index=3}

---

## Important Findings

The study observed that:

- Helix content increases with peptide length
- Small peptides contain more coil regions
- Identical peptide sequences may adopt different structures in proteins

Example observations:

| Sequence | Peptide Structure | Protein Structure |
|----------|------------------|------------------|
| MSRG | CCCC | HHHC |
| YVKA | CCCC | HHHH |
| LDADF | CCCCC | HHHHH |



---

## Best Model Performance

### Binary Profile Model

Random Forest achieved:

- Overall Accuracy (Q3): 81.51%

### PSSM-Based Model

Random Forest achieved:

- Overall Accuracy (Q3): 83.45%

Source: :contentReference[oaicite:5]{index=5}

---

## Balanced Prediction Performance

After applying frequency-based weighting:

### PSSM Random Forest Model

- Helix Accuracy (Q3H): 80.62%
- Sheet Accuracy (Q3E): 74.00%
- Coil Accuracy (Q3C): 87.01%
- Overall Accuracy (Q3): 83.48%

Source: :contentReference[oaicite:6]{index=6}

---

## Comparison with PSIPRED

PEP2D outperformed PSIPRED on peptide datasets.

| Method | Overall Accuracy (Q3) |
|--------|----------------------|
| PSIPRED | 76.86% |
| PEP2D | 83.48% |

### Beta-Sheet Prediction

| Method | Q3E |
|--------|------|
| PSIPRED | 54.37% |
| PEP2D | 74.00% |

Source: :contentReference[oaicite:7]{index=7}

---

## Segment Overlap Measure (SOV)

PEP2D achieved better SOV scores than PSIPRED.

| Method | Overall SOV |
|--------|-------------|
| PSIPRED | 69.35 |
| PEP2D | 76.75 |

Source: :contentReference[oaicite:8]{index=8}

---

## Comparison with PEPstr

PEP2D also outperformed PEPstr.

### PEPstr Performance

- Overall Accuracy: 67.09%

### PEP2D Performance

- Overall Accuracy: 83.48%

Source: :contentReference[oaicite:9]{index=9}

---

## Web Server Features

The PEP2D server allows users to:

- Predict peptide secondary structure
- Submit single or multiple peptide sequences
- View graphical prediction results
- Generate mutant peptides
- Download standalone software

The server provides:

- Helix probability
- Sheet probability
- Coil probability
- Graphical visualization

Source: :contentReference[oaicite:10]{index=10}

---

## Technologies Used

- Random Forest
- ANN
- IBK
- HHblits
- DSSP
- PHP
- HTML
- JavaScript
- Red Hat Linux

---

## Applications

PEP2D can be used for:

- Peptide therapeutics
- Structural bioinformatics
- Drug discovery
- Peptide engineering
- Antimicrobial peptide research
- Rational peptide design

---

## Availability

Web Server:

https://webs.iiitd.edu.in/raghava/pep2d/

---

## Contact

### Prof. Gajendra P. S. Raghava

Department of Computational Biology  
Indraprastha Institute of Information Technology Delhi  
New Delhi, India

Email: raghava@iiitd.ac.in

---

## License

CC-BY-NC-ND 4.0 International License

---
