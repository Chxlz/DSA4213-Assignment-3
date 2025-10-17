# DSA4213 Assignment 3 – Fine-Tuning Transformers

### Author
Rachel Chun
National University of Singapore  
Module: DSA4213 – Advanced Machine Learning for Data Science

---

## Overview
This repository contains the code for Assignment 3 comparing:
- **Full Fine-Tuning**
- **LoRA (r = 4, 8, 16)** on `bert-base-uncased`
for the binary text classification task *Phishing Site Detection*.

---

## Environment Setup
```bash
# Install dependencies
!pip install -q transformers datasets peft accelerate evaluate torch matplotlib scikit-learn
```
---

## Overview
This repository contains the code for Assignment 3 comparing:
- **Full Fine-Tuning**
- **LoRA (r = 4, 8, 16)** on `bert-base-uncased`
for the binary text classification task *Phishing Site Detection*.


| File                             | Description                                                      |
| -------------------------------- | ---------------------------------------------------------------- |
| `DSA4213_Assignment3.ipynb`      | Main Colab notebook with all training, evaluation, and ROC plots |
| `DSA4213_Assignment3.py`         | Clean Python version of the notebook                  |
| `DSA4213_Assignment3_Report.pdf` | Final written report submitted for grading                       |
| `README.md`                      | Instructions for reproduction and reference                      |

---

## Notes on API Keys
Hugging Face and Weights & Biases tokens have been removed for security.
To track runs, insert your own tokens in the notebook where indicated:
```
from huggingface_hub import login
login("YOUR_HF_TOKEN")
import wandb
wandb.login("YOUR_WANDB_KEY")
```

---

## Results Summary

| Model          | Accuracy |   F1   | ROC-AUC |
| :------------- | :------: | :----: | :-----: |
| Full Fine-Tune |  0.9156  | 0.9155 |  0.978  |
| LoRA r = 4     |  0.8556  | 0.8555 |  0.922  |
| LoRA r = 8     |  0.8533  | 0.8533 |  0.923  |
| LoRA r = 16    |  0.8511  | 0.8511 |  0.924  |

---
## How to Reproduce
Clone this repository or open the notebook in Google Colab.
Run all cells — the dataset (shawhin/phishing-site-classification) loads automatically from Hugging Face.

The notebook will:
Train the models (Full, LoRA 4/8/16)
Evaluate metrics (Accuracy, F1, Precision, Recall, ROC-AUC)
Plot the ROC curves for comparison

---

## Environment
Google Colab GPU: NVIDIA T4 (16GB)
Libraries: PyTorch 2.2, Transformers 4.44, PEFT 0.11
Random Seed: 42

---

## Citation
Shawhin (2023). Phishing Site Classification Dataset – Hugging Face.
