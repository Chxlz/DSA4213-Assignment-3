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
