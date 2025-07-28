# App Review Classification using Deep Learning Models

Automated pipeline to classify app store reviews into **bug reports**, **feature requests**, **user experience** and **star ratings** to support Requirements Engineering (RE) activities.  
The project evaluates five representative models – **SVM**, **BERT**, **RoBERTa**, **BART** and **LLaMA** – on both multi‑class *and* multi‑label tasks, under balanced and un‑balanced data regimes.

---

## Table of Contents
1. [Project Highlights](#project-highlights)
2. [Dataset](#dataset)
3. [Quick Start](#quick-start)
4. [Training & Evaluation](#training--evaluation)
5. [Results](#results)
6. [Repository Structure](#repository-structure)

---

## Project Highlights

| Feature | Details |
|---|---|
| **4‑way label schema** | `bug_report`, `feature_request`, `user_experience`, `rating` |
| **Two task types** | Multi‑Class (1 label) & Multi‑Label (≥1 label) |
| **Five models** | SVM, BERT‑base, RoBERTa‑base, BART‑base, LLaMA‑1B |
| **Scalable dataset** | 4 k → 20 k English reviews with manual and GPT labels |
| **State‑of‑the‑art accuracy** | Macro‑F1: 0.996 on 8k samples with BERT/LLaMA (MC); 0.993 on 16k samples with LLaMA (ML) |
| **Reproducible code** | Single YAML/CLI config, PyTorch + Transformers |

---

## Dataset

* **Source** : Hugging Face dataset *PavelGh/app_reviews* (English reviews from Google Play & F‑Droid)  
* **Splits** : 80 % train · 10 % valid · 10 % test (stratified)  
* **Sizes** : 4 k / 8 k / 16 k / 20 k samples  
* **Labels** :

| Task | Balanced? | Label source | Sizes |
|------|-----------|--------------|-------|
| Multi‑Class | ✔︎ / ✘ | Manual + GPT | 4 k / 8 k / 20 k |
| Multi‑Label | ✘ | GPT | 4 k / 8 k / 16 k |

See the report for full details.

---

## Quick Start
...

---

## Training & Evaluation

| Component | Setting |
|-----------|---------|
| Tokenizer length | 256 tokens |
| Optimizer | AdamW |
| Scheduler | Linear with 10 % warm‑up |
| Early‑Stopping | patience = 3  |
| Metrics | Precision, Recall, Macro‑F1, Micro‑F1, Accuracy |

To reproduce *all* experiments run:

...

---

## Results

### Macro‑F1 (mean of 3 runs, GPT‑labelled data)

| Model   | Macro F1 (Multi-class) | Macro F1 (Multi-label) |
|---------|-----------------------|------------------------|
| svm     | 0.779                 | 0.854                  |
| bert    | 0.975                 | 0.926                  |
| roberta | 0.962                 | 0.921                  |
| bart    | 0.941                 | 0.921                  |
| llama   | 0.989                 | 0.886                  |


*MC = Multi‑Class, ML = Multi‑Label. Full tables and plots in report*

---

## Repository Structure

...

---

Enjoy and feel free to reach out via [Issues](../../issues) for any problems or questions!
