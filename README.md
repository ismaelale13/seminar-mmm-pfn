# Causal PFNs for Marketing Mix Modeling

Seminar project on Prior-data Fitted Networks (PFNs) for Marketing Mix Modeling (MMM).

---

## Abstract

This seminar project investigates whether Prior-data Fitted Networks (PFNs) can recover marketing attribution patterns comparable to a Bayesian Marketing Mix Model (MMM) without explicitly specified structural assumptions such as adstock and saturation.

The project compares Bayesian MMM against CausalPFN, TabPFN, and Do-PFN using simulated marketing data. The evaluation focuses on attribution recovery, channel ranking alignment, forecasting performance, and the role of explicit marketing structure in causal attribution modeling.

---

## Research Question

Can PFNs (CausalPFN, Do-PFN, TabPFN) recover comparable channel attribution and ROAS estimates to a Bayesian Marketing Mix Model without explicitly specified structural priors for adstock and saturation - and where do they systematically fall short?

The project further evaluates where PFN-based approaches diverge from the attribution behavior of the Bayesian MMM benchmark.

---

## Repository Structure

- `raw_data/` → original Robyn simulated dataset
- `processed_data/` → cleaned and transformed datasets
- `notebooks/` → model development and comparison notebooks
- `outputs/figures/` → generated plots and visualizations
- `outputs/tables/` → generated result tables
- `code/` → reusable helper scripts and utilities

---

## Notebooks

- `01_data_exploration.ipynb` → exploratory data analysis and preprocessing
- `02_bayesian_mmm.ipynb` → Bayesian MMM benchmark model
- `03_causal_pfn.ipynb` → CausalPFN attribution analysis
- `04_tab_pfn.ipynb` → TabPFN forecasting and attribution analysis
- `05_do_pfn.ipynb` → Do-PFN causal attribution analysis
- `06_comparisons_summary.ipynb` → cross-model comparison and final evaluation

---

## Methodological Overview

### Bayesian MMM
The Bayesian MMM serves as the benchmark model and explicitly models:
- adstock (carryover effects),
- saturation effects,
- channel-level contributions,
- ROAS estimates,
- and posterior uncertainty.

### PFN-Based Models
The project evaluates multiple PFN-based approaches:
- CausalPFN
- TabPFN
- Do-PFN

The goal is to determine whether PFNs can recover marketing attribution structure without manually specified marketing priors.

---

## Main Findings

- Bayesian MMM produced stable and interpretable attribution estimates.
- CausalPFN showed relatively weak attribution recovery, although adstock preprocessing partially improved alignment.
- TabPFN achieved the strongest forecasting performance but weaker attribution recovery.
- Raw Do-PFN achieved the strongest alignment with the Bayesian MMM benchmark without explicitly specified adstock or saturation structure.
- Explicit marketing structure still appears important for stable and interpretable attribution recovery.

---

## Current Status

- Bayesian MMM benchmark completed
- PFN model evaluations completed
- Cross-model comparison completed
- Seminar paper writing in progress

---

## Dataset

The project uses the simulated weekly marketing dataset from Meta Robyn.

---

## Technologies Used

- Python
- PyMC-Marketing
- PyMC
- ArviZ
- TabPFN
- CausalPFN
- Do-PFN
- Pandas
- NumPy
- Matplotlib
- Google Colab
- VS Code

---

## Authors

Seminar project developed as part of a university research seminar by Ismayil Alizada and Sebastian Leipold on causal machine learning and marketing mix modeling.