# Shapes and Colors — Multi-Label Classification (Kaggle-style)

> Notebook viewer: https://nbviewer.org/github/nittinmurthi/kaggle-shapes-and-colors.git/blob/main/shapes-and-colors-report.ipynb


A concise, reproducible repository for a Kaggle-style challenge: predict all (shape, color) pairs present in each image. Shapes: circle, square, triangle. Colors: red, green, blue. Output format matches a typical Kaggle submission: a stringified list of tuples per image.

## Overview
- Task: Multi-label classification over 9 shape–color classes (3 shapes × 3 colors)
- Backbone: ResNet-18 (transfer learning)
- Loss: BCEWithLogitsLoss (multi-label)
- Metrics (test): Jaccard (micro/macro) = 1.000; Precision/Recall/F1 (micro) = 1.000; Per-class F1 = all 1.000
- Notebook:  (end-to-end analysis, training, inference, submission generation)

## Dataset
Place the dataset under:

all-shapes-and-colors-v-2/
  ├─ train_dataset/           # images (not tracked)
  ├─ test_dataset/            # images (not tracked)
  ├─ train.csv                # labels for training (not tracked)
  └─ test.csv                 # image filenames for test (not tracked)

This repo does not include the dataset or model weights. Add them locally using the folder structure above.

## Label Format
Submission requires a stringified Python list of tuples for each image, e.g.:

image_path,label
img_101.png,"[(\'circle\', \'blue\'), (\'square\', \'red\')]"
img_102.png,"[(\'triangle\', \'green\')]"

## Environment
Install Python deps:



If using pyenv/virtualenv, activate your environment first.

## How to Reproduce
1) Open the notebook:



2) Run EDA and training (or load existing weights if available).
3) Run the prediction/submission section. It reads , loads images from , and writes  at the project root.

## Results (Summary)
- Perfect performance on held-out test: all metrics at 1.000.
- Manual review of 50+ samples confirmed label–image alignment.

## Repository Contents
-  — Complete analysis, training, inference pipeline
-  — Minimal environment to run the notebook
-  — Excludes datasets, checkpoints, and large artifacts
-  — This file

## Notes
- Large assets (datasets,  weights, and generated submissions) are ignored by Git.
- Paths in the notebook assume this repository root and the dataset layout above.

## License
This repository contains only code and documentation created for a shapes/colors Kaggle-style challenge. Datasets and model weights are excluded.
