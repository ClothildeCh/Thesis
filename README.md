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
```
### 2. Load best model

Download the Trained Model (v4.1)
The final trained model (version v4.1) is available via Google Drive:
https://drive.google.com/drive/folders/130fC0cXzwM9jx29oo8vzYbfF1Mr2BrjU?usp=sharing

After downloading:
Unzip the folder
Place the contents inside your local models/v4.1/ directory

Ensure the folder contains:
spiece.model
config.json
tokenizer_config.json
special_tokens_map.json

### 3. ACOSQE !

Run inference with src/inference.py
```
python src/inference.py \
  --input_csv data/test_reviews.csv \
  --output_csv outputs/v4.1_predictions.csv \
  --model_path models/v4.1
```

### 4. Evaluation

Model performance is tracked on a fixed 5-review gold test set using:
Exact Match
Quad-level Precision, Recall, F1
Hallucination Rate
Under-generation Analysis
Visual outputs include attention heatmaps and Power BI (hosted on NEST SharePoint - restricted) charts showing extracted aspect distributions.


### Data Disclaimer
The full Trustpilot dataset used for training is not included due to data use limitations.



### Author
Clothilde Charles
MSc Data Science – City, University of London
Supervised by: PRANAVA MADHYASTHA
In collaboration with: National Employment Savings Trust (NEST)
