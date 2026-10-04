# Perception

This folder contains my solutions for Perception Questions 1 and 2.

## Q1 — The Road Disappears

Notebook:

`Q1_Lane_Detection.ipynb`

The notebook contains:

- inspection of clear, shadow and missing-boundary frames
- simple brightness-based lane detection baseline
- baseline evaluation on all 72 frames
- analysis of shadow and false-seam failures
- revised detector using expected road width and temporal information
- confidence values
- MAE and unknown-rate comparison
- failure examples and plots

Run the notebook from top to bottom.

## Q2 — A Crossing with Conflicting Evidence

Notebook:

`Q2_Crossing_Decision.ipynb`

The notebook contains:

- inspection of the three crossing episodes
- baseline GO / SLOW / STOP decision rule
- V2X message-age calculation
- revised decision rule for stale and conflicting evidence
- stopping-distance calculations
- baseline versus revised evaluation
- 20 uncertainty trials using random seed 42
- response-delay and failure analysis

## Requirements

Main packages:

```text
numpy
pandas
matplotlib
opencv-python