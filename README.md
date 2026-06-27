# Duplicate Question Detection

This repository contains the implementation artefact for the final thesis:

**Interpretable and Robust Duplicate Question Detection: A Comparative Study of Classical Features and Transformer-Based Language Models**

Author: **Deepak Kaithwas**  
Programme: **Master of Science in Machine Learning and Artificial Intelligence**  
University: **Liverpool John Moores University – upGrad**

## 1. Project Overview

Online question-answering platforms such as Quora and Stack Overflow often contain multiple questions that express the same intent using different wording. Duplicate question detection is therefore an important Natural Language Processing task because it helps reduce repeated content, improve search quality, and support better user experience.

This project compares classical machine learning techniques and transformer-based language models for duplicate question detection using the Quora Question Pairs dataset.

## 2. Problem Statement

The task is to determine whether two given questions are semantically duplicate. The problem is challenging because two questions can have the same meaning even when they use different vocabulary, sentence structure, or phrasing.

Example:

- Question 1: *How can I lose weight quickly?*
- Question 2: *What are fast ways to reduce body weight?*

Although these questions are lexically different, they are semantically similar and should be detected as duplicates.

## 3. Dataset

The project uses the **Quora Question Pairs** dataset, which contains pairs of questions and a binary label indicating whether the two questions are duplicates.

The dataset is publicly available on Kaggle:

<https://www.kaggle.com/c/quora-question-pairs>

The dataset is **not included in this repository** due to size and licensing considerations. Please download it from Kaggle and place it inside the `data/raw/` directory before running the notebook.

Expected file location:

```text
data/raw/train.csv
```

## 4. Methodology

The implementation follows the research workflow below:

1. Environment setup
2. Data loading and exploration
3. Text preprocessing
4. Feature engineering
5. Train-test split
6. Model training and tuning
7. Model evaluation
8. Comparison of classical and transformer-based approaches

## 5. Models Covered

The notebook includes experiments for:

### Classical Machine Learning Models

- Logistic Regression
- Support Vector Machine / Linear SVM
- Random Forest
- XGBoost

### Feature Engineering

- Bag-of-Words
- TF-IDF
- N-gram features
- Pairwise lexical similarity features
- Fuzzy matching features
- Question length and overlap features

### Transformer-Based Models

- BERT-style pair classification
- Sentence-BERT semantic similarity modelling

The transformer sections may require GPU runtime or cloud notebook execution depending on available hardware.

## 6. Evaluation Metrics

The models are evaluated using standard classification metrics:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix

The thesis also discusses interpretability, robustness, and efficiency as part of the model comparison.

## 7. Repository Structure

```text
duplicate-question-detection/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
│
├── data/
│   └── README.md
│
├── notebook/
│   └── Master_QA.ipynb
│
├── results/
│   ├── figures/
│   ├── metrics/
│   └── confusion_matrices/
│
└── sample_output/
```

## 8. How to Run

### Step 1: Clone the repository

```bash
git clone https://github.com/<your-username>/duplicate-question-detection.git
cd duplicate-question-detection
```

### Step 2: Create a Python environment

```bash
python -m venv .venv
```

Activate the environment:

```bash
# Windows
.venv\Scripts\activate

# macOS/Linux
source .venv/bin/activate
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Download the dataset

Download the Quora Question Pairs dataset from Kaggle and place `train.csv` in:

```text
data/raw/train.csv
```

### Step 5: Run the notebook

Open the notebook:

```text
notebook/Master_QA.ipynb
```

Run the cells sequentially in Jupyter Notebook, JupyterLab, Google Colab, or Kaggle Notebooks.

## 9. Notes for Reproducibility

- Random seed is set in the notebook for reproducibility.
- Classical ML models can usually run on CPU.
- Transformer-based models may require GPU for faster execution.
- If running on limited hardware, use a smaller dataset sample for transformer experiments.

## 10. Thesis Submission Note

This repository is intended as a simple and reproducible implementation companion for the final MSc thesis. It is intentionally kept lightweight and notebook-driven so that the methodology, experiments, and results can be reviewed easily.

## 11. Runing code on Google Colab

<https://colab.research.google.com/drive/1UwkqDWsqIeD6nmv4j99NIdlO77P3Rp0w?usp=sharing>

## 11. Author

**Deepak Kaithwas**  
Master of Science in Machine Learning and Artificial Intelligence  
Liverpool John Moores University – upGrad
