# ML4CHEM — Predicting Blood-Brain Barrier Penetration

Group project for the *Machine Learning for Chemistry* course, inspired by the work of Hirohara et al.

## Project

We work with the **BBBP (Blood-Brain Barrier Penetration)** dataset: about 2,000 small molecules, each labeled with a binary indicator for whether the compound can cross the blood-brain barrier. The goal is to predict this property directly from the molecule's SMILES string.

We approach the task in two ways and compare them:

1. A **convolutional neural network (CNN)** trained from scratch, operating on character-level SMILES.
2. **ChemBERTa-77M-MTR**, a transformer pre-trained on 77M molecules from PubChem, fine-tuned for BBBP classification.

The central question: can a pre-trained chemical language model outperform a CNN trained from scratch on a small dataset like BBBP?

## Notebooks

- **Exploratory data analysis** — [`notebooks_EDA/01_eda.ipynb`](https://github.com/elhartw/ML4CHEM/blob/main/notebooks_EDA/01_eda.ipynb)
- **CNN from scratch** — [`CNN_BBBP.ipynb`](https://github.com/elhartw/ML4CHEM/blob/main/CNN_BBBP.ipynb)
- **ChemBERTa fine-tuning** — [`chemberta_bbbp_improved_fixed.ipynb`](https://github.com/elhartw/ML4CHEM/blob/main/chemberta_bbbp_improved.ipynb)

## Dataset

BBBP is part of the [MoleculeNet](https://moleculenet.org/) benchmark suite and is publicly available via DeepChem. Each molecule has a SMILES string and a binary label `p_np` (1 = penetrates, 0 = does not). The class distribution is imbalanced (~76% positive), which we address through scaffold-based splitting and class-weighted loss.
