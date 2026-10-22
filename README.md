# ECE32 — Machine Learning Capstone (Group 4)

**Predicting At-Risk Students from Social and Behavioral Factors: A Machine Learning Approach to Early Academic Intervention**

IC-ML: Machine Learning · University of Santo Tomas — Faculty of Engineering, Electronics Engineering Department

## Group 4
Khalil Badal · Amiel Elestin Cruz · Sherman Lloyd Ko · Elijah David Lopez · Klein Isshi Trangia · Arc Joseph Villarmil

## Overview
This capstone develops a machine learning **classification** solution that identifies secondary-school
students **at risk of failing** the final grade, so that educators can intervene early. The problem is
framed as binary classification: a student is labeled *at risk* when the final grade (G3) falls below the
passing mark of 10.

A central question is **how early** risk can be detected. The two interim period grades (G1, G2) are strong
predictors of the final grade but only appear partway through the term, so the models are evaluated under
**two scenarios** — *with* and *without* G1/G2 — to measure how much the interim grades contribute and how
well a student can be flagged from earlier, non-grade factors alone.

## Dataset
[UCI Student Performance Dataset](https://archive.ics.uci.edu/dataset/320/student+performance) (mathematics subset):
395 students, 33 attributes, binary pass/fail target. The classes are imbalanced (~1 in 3 fail). See `data/`.

## Approach
- **Models:** Logistic Regression · K-Nearest Neighbors · Support Vector Machine
- **Feature analysis:** feature selection, recursive feature elimination, and PCA
- **Evaluation:** recall, precision, F1-score, confusion matrix, and ROC-AUC (with emphasis on recall for
  the minority at-risk class); cross-validation for robustness
- **Tools:** Python (Spyder), pandas, scikit-learn, Matplotlib/Seaborn

## Objectives
1. Train and compare classification models (KNN, Logistic Regression, SVM) to identify students at risk of failing.
2. Compare performance with and without the interim grades (G1, G2) to measure their contribution.
3. Apply feature selection and dimensionality reduction to find the most influential factors.
4. Evaluate and compare the models with appropriate metrics and validation, prioritizing recall and F1.
5. Deliver a documented, reproducible Python implementation as a prototype early-warning tool.

## Repository structure
```
docs/   Proposal paper, presentation slides, and defense kit
data/   UCI Student Performance dataset and description
```

- `docs/Group4_Capstone_Proposal.docx` — 4-page IEEE proposal
- `docs/Group4_Proposal_Slides.pdf` — proposal presentation slides
- `docs/Group4_Presentation_Kit.docx` / `.pdf` — speaker script and panel Q&A prep
- `data/student-mat.csv` — dataset (semicolon-separated)
- `data/student.txt` — attribute descriptions
- `data/student-merge.R` — dataset merge helper

## Status
- [x] **Prelims:** Capstone proposal (paper + slides + presentation)
- [ ] **Finals:** Python implementation, model training and comparison, evaluation, and final paper

---
*Course: IC-ML Machine Learning · First Term, AY 2026–2027*
