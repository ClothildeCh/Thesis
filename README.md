# Aspect-Based Sentiment Analysis of NEST Trustpilot Reviews using ACOSQE

This repository contains the code, resources, and evaluation materials for my MSc Data Science dissertation project at City, University of London in collaboration with NEST (National Employment Savings Trust). The project focuses on **Aspect-Category-Opinion-Sentiment Quadruple Extraction (ACOSQE)** using transformer-based models to provide actionable insights into customer reviews from Trustpilot.

---

## Project Summary

The goal of this project is to move beyond traditional document-level sentiment analysis and extract fine-grained opinion structures from reviews, structured as **(aspect, category, opinion, sentiment)**. This enables NEST and similar pension providers to identify key themes, pain points, and strengths in customer feedback.

I fine-tuned T5-based models using a manually annotated dataset of over 1000 reviews. The final outputs are evaluated against a fixed gold test set and visualised in Power BI.

---

##  How to Run the Code

### 1. Install Dependencies

```bash
pip install -r requirements.txt

### 2. Load best model

best_model_v4;zip

### 3. ACOSQE !

### 4. Evaluation
Model performance is tracked on a fixed 5-review gold test set using:
Exact Match
Quad-level Precision, Recall, F1
Hallucination Rate
Under-generation Analysis
Visual outputs include attention heatmaps and Power BI charts showing extracted aspect distributions.


Data Disclaimer
The full Trustpilot dataset used for training is not included due to data use limitations.



Author
Clothilde Charles
MSc Data Science – City, University of London
Supervised by: 
In collaboration with: National Employment Savings Trust (NEST)
