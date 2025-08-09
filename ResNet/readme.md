# ResNet — Deeper Network Experiments (PyTorch)
## Overview
This notebook contains experiments using a ResNet-style architecture (either a custom small ResNet or a torchvision.models ResNet such as resnet18) to train on CIFAR-type data. It demonstrates training loops, validation, plotting, and basic model inspection.

## Files
ResNet.ipynb — Main notebook:

 - Model definition or torchvision model usage

 - Dataset loading and preprocessing

 - Training & validation loops, checkpoint saving

Performance visualization and optional model summaries (torchinfo)

## Dataset
- CIFAR-10 via torchvision.datasets.CIFAR10 is recommended for small-scale experiments.

- For custom datasets, add a download_dataset.py or a clear dataset/README.md describing layout.

## How to run
1.Install dependencies:

```bash
Copy code
pip install -r ../requirements.txt
Open ResNet.ipynb in Jupyter/Colab/VSCode.
```
2.If available, use GPU (device = 'cuda') and run cells top-to-bottom.

3.Use smaller epochs for quick checks; scale up for final runs.

## Example hyperparameters (update from notebook)
- Model: resnet18 (or custom ResNet-blocks)
- Epochs: 50
- Batch size: 128
- Optimizer: SGD with momentum (lr=0.1, momentum=0.9), plus StepLR or cosine scheduler
- Weight decay: 5e-4
- Seed: 42

## Expected outputs:

- Training / validation loss and accuracy curves
- Final test accuracy and per-class metrics
- Model summary (parameter count)

## Reproducibility & improvements
Reproduce by setting seed, saving config dict, and loading models/best_resnet.pt.

## Improvements to try:

- MixUp / CutMix data augmentation
- Label smoothing
- Sweep learning rates and optimizer types

## Credits
- ResNet: He et al., "Deep Residual Learning for Image Recognition"
- Dataset: CIFAR-10 (if used)
