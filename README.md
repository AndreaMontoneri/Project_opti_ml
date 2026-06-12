# Project_opti_ml
This repository contains the codebase for the CS-439 Optimization for Machine Learning project.

The project was developed by **Léon L'Huillier, Florian Tanguy, and Andrea Montoneri.**

## Reproducibility

All figures, tables, and numerical results shown in the final report were generated all from the notebook `SGD_HD.ipynb` 

To fully reproduce the report:

1. Open the notebook.
2. Execute all cells in order from top to bottom
3. Do not skip cells, as later sections depend on variables, models, and outputs created earlier.

> **Reproducibility Note:** All random seeds are fixed and all hyperparameters are explicitly specified.
> Running **Cell → Run All** reproduces every figure and result used in the report.

## Automatic Recovery & Persistence

Execute the first three setup cells to set-up the whole notebook

These cells:

- Enable anti-idle functionality for long-running experiments.
- Mount Google Drive for  storage.
- Automatically restore saved checkpoints and progress.

## Hardware Configuration

The variable `DEVICE` automatically selects a GPU when one is available. This is particularly important for CIFAR-10 experiments, which are significantly slower on CPU.

The constant `SEED` ensures that all stochastic operations are reproducible, including:

- Weight initialization
- Data shuffling
- Random sampling
- Dropout operations

As a result, repeated executions produce consistent results across runs.