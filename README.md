# An Introductory Guide to Artificial Intelligence for Engineers

Companion code for the guide: **An Introductory Guide to Artificial Intelligence for Engineers**.

This repository contains the Jupyter notebooks and supplementary materials needed to follow along with each chapter. The guide presents core AI/ML concepts through practical, engineer-oriented case studies.

## Repository Contents

| File | Description |
|------|-------------|
| `AIforEngineers.pdf` | Full guide (PDF) |
| `ch2_LinearRegression.ipynb` | **Linear Regression** — Predicting elastic stress from strain using closed-form solutions and gradient descent |
| `ch3_SymbolicRegression.ipynb` | **Symbolic Regression** — Discovering closed-form beam-deflection equations via genetic programming |
| `ch4_NeuralNetworks.ipynb` | **Neural Networks** — Binary image classification for concrete crack detection (FNN and CNN) |

## Getting Started

The notebooks are designed to run in [Google Colab](https://colab.research.google.com) with no local setup required. To run locally, install the dependencies below.

### Dependencies

| Notebook | Key Packages |
|----------|-------------|
| Chapter 2 | NumPy, Matplotlib |
| Chapter 3 | NumPy, Pandas, Matplotlib, SymPy, gplearn |
| Chapter 4 | NumPy, Matplotlib, Seaborn, PyTorch, torchvision, scikit-learn |

Install all dependencies at once:

```bash
pip install numpy matplotlib seaborn pandas sympy gplearn torch torchvision scikit-learn
```

## Citation

If you use this guide or its accompanying code, please cite:

**BibTeX**

```bibtex
@misc{smith2026aiforengineers,
  author    = {Smith, Sam},
  title     = {An Introductory Guide to Artificial Intelligence for Engineers},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.18728345},
  url       = {https://doi.org/10.5281/zenodo.18728345}
}
```

**IEEE**

> S. Smith, "An Introductory Guide to Artificial Intelligence for Engineers," Zenodo, 2026. doi: 10.5281/zenodo.18728345.

