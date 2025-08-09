# ANN — From-scratch Neural Networks (NumPy)

## Overview
This notebook implements small neural networks from scratch using NumPy. The experiments focus on simple supervised learning tasks such as binary logical operations (XOR, AND, OR). The goal is educational: to demonstrate forward pass, backward propagation, activation functions, and a training loop without using frameworks like PyTorch or TensorFlow.

## Files
- `ANN.ipynb` — Main notebook containing:
  - Dataset generation for logical gates
  - Activation functions and their derivatives
  - Neural network class (forward & backward)
  - Training loop, loss/accuracy plots
- `requirements.txt` — Refer to root requirements or install `numpy` and `matplotlib`.

## Dataset
- Synthetic datasets are generated inside the notebook (no external download required).
- Data format: small arrays (X inputs, y labels) for logic gates.

## How to run
1. Install dependencies:
   ```bash
   pip install -r ../requirements.txt
   # or at minimum:
   pip install numpy matplotlib
   ```
2.Open `ANN.ipynb` in Jupyter Lab / Notebook or VSCode and run cells top-to-bottom.
3.Adjust hyperparameters in the config cell if present (learning rate, epochs, seed).

## Expected results
- Training and test losses for each logic-gate experiment.
- Plots of loss and accuracy over training epochs.

## Suggestions & improvements
- Consider converting key functions to a Python `.py` module for reuse and importing into the notebook.
- Add short docstring the top explaining inputs/outputs and hyperparameters.
-Save experiment configurations (learning rate, epochs, seed) to a small config dict and log them to a CSV for reproducibility. 
- Add unit tests for small helper functions (e.g., activation derivatives).
