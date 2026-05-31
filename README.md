# LASO: Local Adaptive Synthetic Oversampling

LASO (Local Adaptive Synthetic Oversampling) is a synthetic oversampling method for multiclass imbalanced classification. The method aims to generate more representative minority samples by incorporating local neighborhood structure and local manifold information through localized principal component analysis (PCA).

This repository contains the reference Jupyter Notebook implementation used for experimental evaluation and benchmarking against several classical and state-of-the-art oversampling methods.

## Features

* Supports multiclass imbalanced datasets.
* Local neighborhood analysis using k-nearest neighbors.
* Local PCA-based manifold approximation.
* Adaptive synthetic sample generation.
* Evaluation pipeline for multiple classifiers and resampling methods.
* Statistical analysis using Friedman and Nemenyi tests.
* Runtime benchmarking using Dolan–Moré performance profiles.
* Failure analysis and robustness reporting.

## Repository Structure

```text
resample_dn_**.ipynb       Main implementation and experiments
data.all/                  Input datasets (not included)
results.all/               Generated outputs
```

## Requirements

The implementation was developed using Python 3.x and relies on commonly used scientific computing libraries. Install dependencies using:

```bash
pip install -r requirements.txt
```

## Running the Experiments

Open the notebook:

```bash
jupyter notebook resample_dn_**.ipynb
```

Configure:

* Dataset directory
* Classifier list
* Resampling methods
* Output directory

Then execute all cells.

The pipeline will automatically:

1. Load datasets.
2. Apply train/test splitting.
3. Perform oversampling.
4. Train classifiers.
5. Evaluate classification performance.
6. Generate statistical comparison tables.
7. Produce runtime benchmarking plots.
8. Export Excel summaries.

## Output

The experiment pipeline generates:

* Classification metrics (Accuracy, Precision, Recall, F1, G-Mean)
* Runtime statistics
* Friedman test results
* Nemenyi post-hoc comparisons
* Dolan–Moré performance profiles
* Failure logs and robustness summaries
* Visualization grids of resampled datasets