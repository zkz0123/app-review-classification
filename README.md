# Experiment Notebooks Backup

This branch contains a backup of all original Jupyter Notebooks used during the initial experimental phase of the app review classification project. These notebooks were used for prototyping and evaluating different models under two classification settings: **multi-class** and **multi-label**.

## Overview

The experiments focused on classifying app reviews into one or more of the following categories:

- Bug reports  
- Feature requests  
- User experience  
- Rating comments

Two types of classification tasks were considered:

- **Multi-class**: each review is assigned to exactly one category  
- **Multi-label**: each review can be assigned to multiple categories simultaneously

## Models Used

The following models were applied and evaluated under both task types:

- **SVM**  
- **BERT**  
- **RoBERTa**  
- **BART**  
- **LLaMA**

## Files Included

This backup includes the following raw notebooks:

- lab_llm(class).ipynb
- lab_llm(labels).ipynb
- lab_svm(class).ipynb
- lab_svm(label).ipynb
- lab(class).ipynb
- lab(label).ipynb 

These notebooks contain original code for data loading, preprocessing, model training, evaluation, and preliminary result analysis. Note that some code may be redundant or tightly coupled across tasks and models, as these notebooks were designed for experimentation rather than modular reuse.

## Purpose of This Branch

This `backup` branch is intended solely for preserving the original notebooks as a reference. Future development has been modularized and is maintained in structured source code across feature branches (e.g., `model/bert`, `task/multilabel`, etc.).

---
