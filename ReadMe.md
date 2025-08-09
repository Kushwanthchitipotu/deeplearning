# Deep Learning Projects

A curated collection of small-to-medium deep learning notebooks and experiments.  
Each project is isolated in its own folder with a project-specific `README.md` explaining goals, how to run it, and key results.

---

## Repository overview

This repository is designed to showcase practical experiments with neural networks, from-scratch NumPy implementations to PyTorch CNN and ResNet experiments using open datasets. It is intended as a learning portfolio and a reproducible research folder.

### Projects
| Folder | Short description |
|--------|-------------------|
| `ANN/`   | From-scratch neural networks (NumPy) — logical gates, training loop, and visualization. |
| `CNN/`   | PyTorch CNN experiments — baseline architecture, dropout, batchnorm; CIFAR-style dataset. |
| `ResNet/`| ResNet-style experiments using PyTorch / torchvision for deeper models. |

---

## Quick start

1. Clone the repo:
```bash
git clone https://github.com/Kushwanthchitipotu/deeplearning.git
cd deeplearning
```
2.(Optional) Create and activate a virtual environment:

```bash
python -m venv venv
# macOS / Linux
source venv/bin/activate
# Windows (PowerShell)
venv\Scripts\Activate.ps1
```
3.Install dependencies:
```bash
pip install -r requirements.txt
```
4.Open notebooks:

Launch Jupyter Lab / Jupyter Notebook or open the folder in VSCode.

Open and run notebooks inside each project folder (run cells top-to-bottom).

For GPU runs, use a CUDA-enabled machine or open notebooks in Google Colab.

## Recommended workflow
- Work and iterate locally in a private branch (or private repo) while the course is active.

- When ready to publish a polished version:

  - Clean notebooks (remove exact assignment text if needed).

  - Add a project-level README.md (each project folder should have one).

  - Add results (plots, confusion matrices) and a short “What I learned” section.

- Keep large datasets and model weights out of the repo — use .gitignore (see .gitignore file).

## Reproducibility tips
- Add a small config cell near the top of notebooks with hyperparameters and random seed (e.g., seed = 42).

- Save best checkpoints during training and log final metrics to a JSON/CSV.

- If a notebook depends on a dataset, either include a small download script or clear instructions to obtain the data.


## Notes & licensing
- If you want others to reuse your code, add a license (MIT or Apache-2.0 are common choices).

- Use .gitignore to avoid committing large files like raw datasets and model weights.

- Give credit for datasets and references in each project README.md.


## Credits

These projects were completed as part of coursework under the supervision of Professor Sumohana Channappayya (Electrical Department) during deeplearning AI2100 at IIT Hyderabad.
 

## Contact / Author
Kushwanth Ch — GitHub: Kushwanthchitipotu

