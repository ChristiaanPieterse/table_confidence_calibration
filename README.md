# Table Confidence Calibration: Dataset & Artifacts

This repository contains the dataset and trained model artifacts for the neuro-symbolic Intelligent Document Processing (IDP) architecture developed at Stellenbosch University. It provides the necessary data to reproduce the statistical evaluations and calibration curves discussed in the associated research.

## Overview
Standard industrial OCR heuristics often suffer from artificial ceiling effects and fail to recognize structural fractures in tabular data. This repository provides the structural feature dataset extracted from scientific documents, allowing researchers to evaluate tabular extraction confidence via explicit structural signals and dynamic calibration.

## Repository Structure
* `data/`: Contains the evaluation dataset (`N = 1,312` annotated table instances) featuring the 17-dimensional structural metrics, baseline vendor OCR confidences, and out-of-fold probability predictions.
* `models/`: Contains the fitted parametric Platt scaling calibrator weights/model file used to map raw log-odds to continuous probabilities.
* `documents/`: Contains the inventory of source PDF filenames and relevant raw document metadata used to compile the dataset.

## Citation
If you utilize this dataset in your research, please cite the associated manuscript:
```bibtex
@article{Pieterse2026Calibration,
  title={Towards trustworthy confidence calibration in tabular extraction},
  author={Pieterse, Christiaan J. and Venter, PvZ},
  journal={...},
  year={2026}
}
