# Confidence Calibration for Structure-Aware Table Extraction

This repository provides the evaluation suite and statistical confidence calibration methods for the neuro-symbolic Intelligent Document Processing architecture. It includes the raw dataset PDF's, trained model and weights needed to reproduce the statistical evaluations, calibration curves, and reliability diagrams discussed in the associated research.

## Overview
Standard industrial OCR heuristics often suffer from artificial ceiling effects and fail to recognize structural fractures in tabular data. This framework lets researchers evaluate tabular extraction confidence using explicit structural signals and dynamic calibration, bypassing traditional flawed heuristics.

## Dataset access (GitHub Releases)
To prevent repository bloat, the static raw PDF evaluation corpus is distributed via GitHub Releases rather than tracked in the version history. 

1. Navigate to the **Releases** section on the right-hand sidebar of this repository.
2. Download the `raw_pdfs.zip` asset from the `v1.0-data` release.
3. Extract the contents directly into the `documents/` directory before executing the pipeline.

## Repository structure
* `data/`: Contains the evaluation dataset (`N = 1,312` annotated table instances) featuring the 17-dimensional structural metrics, baseline vendor OCR confidences, and out-of-fold probability predictions.
* `models/`: Contains the fitted parametric Platt scaling calibrator weights used to map raw log-odds to continuous probabilities.
* `documents/`: Contains the inventory of source PDF filenames and relevant raw document metadata used to compile the dataset. **(Ensure `raw_pdfs.zip` is extracted here).**

## Citation
If you utilize this framework or dataset in your research, please cite the associated manuscript:
```bibtex
@article{Pieterse2026Calibration,
  title={Towards trustworthy confidence calibration in tabular extraction},
  author={Pieterse, Christiaan J. and Venter, PvZ},
  journal={...}, # To be announced
  year={2026}
}
