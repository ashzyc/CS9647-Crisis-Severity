# CS9647-Crisis-Severity
## Overview

This project develops a multi-class text classification pipeline to detect **mental health risk levels** (low, medium, high) from Reddit posts. The goal is to evaluate how well different modelling approaches capture varying levels of distress in their texts.

---

## Structure

- **Data Preprocessing**  
  Raw Reddit posts are cleaned, combined (title + body), filtered, and deduplicated. A balanced dataset is created to ensure fair representation across all classes.

- **Baseline Model (TF-IDF + Logistic Regression)**  
  A traditional machine learning baseline using TF-IDF features and Logistic Regression is implemented to establish a performance benchmark.

- **Transformer Models (BERT & RoBERTa)**  
  Fine-tuned transformer models are used to capture contextual language patterns and improve classification performance. They are great for data like this!

- **Evaluation & Analysis**  
  Models are evaluated using accuracy, macro F1-score, confusion matrices, and error analysis to understand performance differences across classes.

---

## Key Findings

- The baseline model achieves around **64% accuracy**, providing a strong reference point.  
- The **medium-risk class is the most challenging**, since it often overlaps with both low and high-risk posts.  
- Transformer-based models DO show improvements by better capturing contextual meaning.

---

## Note

This result is slightly different from the one submitted in the report due to randomness in preprocessing and training. The issue has since been addressed by ensuring deterministic file ordering during preprocessing (e.g., using `sorted(os.listdir(...))`). The overall trends and conclusions remain consistent!!
