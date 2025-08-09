# CNN — PyTorch Convolutional Neural Networks

## Overview
This notebook compares multiple small CNN architectures (baseline CNN, CNN + dropout, CNN + batch normalization) trained on a CIFAR-like dataset. It explores how architectural choices and regularization affect training stability and generalization.

## Files
CNN.ipynb — Main notebook:

Data loading / augmentation (uses torchvision if available)

Model definitions (SimpleCNN, SimpleCNNWithDropout, SimpleCNNWithBN, etc.)

Training & validation loops

Accuracy / loss plots and sample predictions

dataset/ — (optional) local dataset files. Prefer programmatic download.

## Dataset
Default: CIFAR-10 via torchvision.datasets.CIFAR10 (or a custom CIFAR-like folder).

To download programmatically: see code cell that calls torchvision.datasets.CIFAR10(root='dataset/', download=True, ...).

## How to run
1.Install dependencies:

```bash
Copy code
pip install -r ../requirements.txt
Open CNN.ipynb in Jupyter/Colab/VSCode.
```
2.(Optional) On Colab enable GPU: Runtime → Change runtime type → GPU.

3.Run cells top-to-bottom. Ensure device = 'cuda' is set if GPU is available.

## Example hyperparameters (update with notebook values)
- Epochs: 30
- Batch size: 64
- Optimizer: Adam (lr=0.001) or SGD (lr=0.01, momentum=0.9)
- Augmentation: random crop, random horizontal flip
- Seed: 42

## Checkpoints & outputs
- Save best model to models/best_cnn.pt using torch.save.
- Expected outputs in the notebook:
- Training / validation loss and accuracy curves
- Confusion matrix and per-class accuracy



## Observed effects:
- Dropout improves generalization slightly when overfitting occurs.
- BatchNorm stabilizes and speeds up training.
- If dataset is large, use smaller epochs locally, then run full experiments on GPU.

## Reproducibility & improvements
To reproduce exactly: set seed, use the same augmentation pipeline, and load the same checkpoint.

## Improvements to try:

- Learning rate scheduling (StepLR, ReduceLROnPlateau)
- More extensive augmentation (MixUp, Cutout)
- More training epochs and model checkpointing

## Credits
- Dataset: CIFAR-10 (if used) — Krizhevsky, Hinton et al.
- Inspired by standard PyTorch tutorials and educational resources.
