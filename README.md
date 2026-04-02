# NLP_Assignment_BERT
## Overview
This project demonstrates **fine-tuning a pre-trained BERT model** for sentiment analysis on the **IMDB Movie Reviews dataset**. The goal is to classify movie reviews as **positive** or **negative**.

Pipeline:  
**Raw Data → Preprocessing → Tokenization → Model Training → Evaluation → Analysis & Insights**

---

## Dataset
- Source: [Kaggle – IMDB Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)  
- Total Reviews: 50,000 (balanced positive & negative)  
- Split:  
  - Train: 35,000  
  - Validation: 7,500  
  - Test: 7,500  

---

## Preprocessing
- Removed missing values  
- Converted sentiment labels to numerical:  
  - Positive → 1  
  - Negative → 0  

---

## Tokenization
- Tokenizer: `bert-base-uncased`  
- Max Length: 256  
- Padding: Applied for uniform input length  

---

## Model
- Pre-trained model: **BERT (bert-base-uncased)**  
- Task: Sequence Classification (`num_labels=2`)  
- Training:  
  - Optimizer: AdamW  
  - Learning Rate: 2e-5  
  - Batch Size: 8  
  - Epochs: 2  

---

## Evaluation Metrics
- **Accuracy:** 0.475  
- **Precision:** 0.556  
- **Recall:** 0.047  
- **F1 Score:** 0.087  
- **Confusion Matrix:**

[[ 90   4] [101   5]]

> Note: Model performance can be improved by fine-tuning more epochs, experimenting with batch size, or using models like DistilBERT.

---

## Insights
- Model struggles to detect negative reviews (high false negatives)  
- Freezing vs. fine-tuning BERT layers affects performance  
- Proper preprocessing and tokenization are critical for performance  

---

## How to Run
1. Clone repository:  
```bash
git clone https://github.com/username/NLP-Assignment-BERT.git

2. Install dependencies:



pip install torch transformers scikit-learn pandas

3. Open the notebook: NLP_Task4_BERT.ipynb and run all cells.


If you want, I can also make a **shorter version optimized for GitHub README file**. Do you want me to do that?
