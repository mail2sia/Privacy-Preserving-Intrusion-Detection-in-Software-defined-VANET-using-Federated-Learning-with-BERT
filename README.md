# Privacy-Preserving Intrusion Detection in Software-defined VANET using Federated Learning with BERT

This repository implements the **FL-BERT** model—a novel approach to intrusion detection in Software-defined Vehicular Ad-hoc Networks (VANETs) using **Federated Learning** and **BERT**. The model is designed to ensure strong detection performance while preserving user data privacy.

## Overview

Vehicular Ad-hoc Networks (VANETs) are integral to smart transportation systems. However, their decentralized and dynamic nature makes them vulnerable to various cyberattacks. This project introduces **FL-BERT**, a privacy-preserving Intrusion Detection System (IDS) that:

- Trains a BERT model in a federated learning setting (no data sharing across nodes)
- Detects malicious behavior using VeReMi dataset attack patterns
- Outperforms traditional ML-based IDS approaches

## Features

- **Privacy-Preserving Federated Learning** (FL)
- **Context-Aware Detection** via BERT
- **Superior Accuracy** over SVM, RF, LR, KNN, etc.
- **Benchmark Dataset**: VeReMi (Vehicular Reference Misbehavior dataset)

## Project Structure

```text
.
├── data/                    # Folder to store VeReMi dataset
├── preprocess.py           # Preprocess the dataset
├── train_federated.py      # Main federated training logic using BERT
├── evaluate.py             # Evaluation scripts
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

## Getting Started

### Prerequisites

Install Python dependencies:

```bash
pip install -r requirements.txt
```

### Dataset

Download the [VeReMi dataset](https://veremi-dataset.github.io/) and place the relevant files in the `data/` directory. Follow preprocessing instructions below.

### Run Pipeline

```bash
# Step 1: Preprocess data
python preprocess.py

# Step 2: Train FL-BERT model
python train_federated.py

# Step 3: Evaluate results
python evaluate.py
```

## Results Summary

| Model                  | Accuracy |
|------------------------|----------|
| Random Forest          | 49%      |
| Support Vector Machine | 59%      |
| Logistic Regression    | 59%      |
| K-Nearest Neighbors    | 38%      |
| **FL-BERT (ours)**     | **84%**  |

### Example F1 Scores by Attack Type

- Constant Attack: **1.00**
- Constant Offset Attack: **0.75**
- Eventual Stop Attack: **0.86**

## Citation

If you use this work in your research, please cite it as follows:

### APA

> Ahsan, S. I., Legg, P., & Alam, S. M. I. (2024). *Privacy-Preserving Intrusion Detection in Software-defined VANET using Federated Learning with BERT*. arXiv. https://arxiv.org/abs/2401.07343

### IEEE

> S. I. Ahsan, P. Legg, and S. M. I. Alam, "Privacy-Preserving Intrusion Detection in Software-defined VANET using Federated Learning with BERT," *arXiv preprint arXiv:2401.07343*, 2024. [Online]. Available: https://arxiv.org/abs/2401.07343

### BibTeX

```bibtex
@article{ahsan2024privacy,
  title={Privacy-Preserving Intrusion Detection in Software-defined VANET using Federated Learning with BERT},
  author={Ahsan, Shakil Ibne and Legg, Phil and Alam, S M Iftekharul},
  journal={arXiv preprint arXiv:2401.07343},
  year={2024},
  url={https://arxiv.org/abs/2401.07343}
}
```

### MLA

> Ahsan, Shakil Ibne, Phil Legg, and S. M. Iftekharul Alam. "Privacy-Preserving Intrusion Detection in Software-defined VANET using Federated Learning with BERT." *arXiv preprint arXiv:2401.07343* (2024).


