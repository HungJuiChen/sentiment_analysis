# Sentiment Analysis - IE4483 Artificial Intelligence and Data Mining

## Overview
This project is a sentiment analysis model developed as part of the **IE4483: Artificial Intelligence and Data Mining** course at the **School of Electrical and Electronic Engineering, Academic Year 2023/24, Semester 1**. The project focuses on classifying sentiments in textual data using **DistilBERT**, a lightweight version of BERT, with **subword tokenization** for improved handling of out-of-vocabulary words.

## Project Structure
- **Report**: [IE4483_Artificial_Intelligence_and_Data_Mining_Report.pdf](./IE4483_Artificial_Intelligence_and_Data_Mining_Report.pdf) – Contains a detailed explanation of feature selection, model architecture, training strategy, and model performance.
- **Notebook**: [sentiment_analysis.ipynb](./sentiment_analysis.ipynb) – Jupyter Notebook used for data processing, model training, and evaluation.
- **Submission File**: [submission.csv](./submission.csv) – Output file containing the model's predictions on test data.

## Features
- **Tokenization Strategy**: Utilizes **subword tokenization (WordPiece)** for better word representation.
- **Pretrained Model**: **DistilBERT**, fine-tuned for sentiment classification.
- **Training Strategy**:
  - **Dataset split**: 70% training, 15% validation, 15% testing.
  - **Loss Function**: Cross-entropy loss.
  - **Optimization**: Early stopping with learning rate tuning.
- **Performance Metrics**:
  - **Accuracy**: Improved from **84.34% (pre-training)** to **93.88% (post-training)**.
  - **ROC-AUC**: Increased from **0.9280 to 0.9628**.

## Installation & Usage
### Prerequisites
Ensure you have the required dependencies installed:
```bash
pip install transformers pandas scikit-learn torch
```

### Running the Code
1. Clone the repository and navigate to the project directory:
   ```bash
   git clone <repo-link>
   cd <repo-name>
   ```
2. Open the Jupyter Notebook `sentiment_analysis.ipynb` and run all cells sequentially.

Alternatively, you can run the notebook on Google Colab:
[Google Colab Link](https://colab.research.google.com/drive/1IXtTGuPSR0gYUQMRjJiQc2x-W2Zl7ZlM?usp=sharing)

## Model Performance
| Stage        | Loss  | Accuracy | ROC AUC |
|-------------|-------|----------|---------|
| Pre-training | 0.6592 | 84.34% | 0.9280  |
| Post-training | 0.1598 | 93.88% | 0.9628  |

## Strengths & Limitations
### Strengths
✔️ Effective sentiment classification with **high accuracy**  
✔️ **Subword tokenization** helps with OOV words  
✔️ Utilizes **pretrained transformer models**, reducing training time  

### Limitations
⚠️ Misclassification of nuanced or sarcastic sentiments  
⚠️ Slight variance in results due to **dropout layers** in BERT  

## Contributors
- **Chen Hung-Jui** (U2020125F)
- **Ivan Tan Kah Keng** (U2123310H)
- **Wong Yu Hao** (U2120641H)

## References
Refer to the [project report](./IE4483_Artificial_Intelligence_and_Data_Mining_Report.pdf) for full citations and methodology details.
