# ML4CHEM

Group project for the Machine Learning for Chemistry course.
We predict whether a molecule can cross the blood-brain barrier,
using the BBBP dataset from MoleculeNet.

## What's in this repo

- `notebooks/` — Jupyter notebooks for data exploration and experiments.
- `src/` — Python files with reusable code (CNN model, data loading, training).
- `data/` — Where `BBBP.csv` goes. Not on GitHub, download it yourself.
- `results/` — Plots and trained models.

## How to get started

1. Clone the repo: `git clone https://github.com/elhartw/ML4CHEM.git` and `cd ML4CHEM`
2. Create a virtual environment (a separate Python setup just for this project): `python -m venv .venv`
3. Activate it: `source .venv/bin/activate` on Mac/Linux, or `.venv\Scripts\activate` on Windows
4. Install packages: `pip install -r requirements.txt`
5. Download `BBBP.csv` from [MoleculeNet](https://moleculenet.org/datasets-1) and put it in `data/`
6. Open `notebooks_EDA/01_eda.ipynb` to get started

## Working together

Run `git pull` before you start, and `git push` when you're done.
Avoid working on the same file at the same time.