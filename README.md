# Predicting Beta-Lactam Resistance in *Escherichia coli* Using a Protein Language Model

# Overview
This repository contains the implementation of my Final Year Project (FYP), which focuses on predicting beta-lactam antibiotic resistance in *Escherichia coli* using a Protein Language Model (ProtBERT) and a Random Forest classifier. The project demonstrates how deep learning-based protein embeddings can be combined with traditional machine learning techniques to identify antimicrobial resistance from protein sequences.


# Project Objectives
1 Predict beta-lactam resistance in *E. coli* protein sequences.
2 Generate contextual protein embeddings using the pretrained ProtBERT model.
3 Train a Random Forest classifier for resistance prediction.
4 Evaluate model performance using multiple classification metrics.
5 Perform virtual mutation analysis to investigate the effect of amino acid substitutions on predicted resistance.


# Dataset
The protein sequence dataset was obtained from the **Pathosystems Resource Integration Center (PATRIC)** database.
The dataset consists of:
1 Resistant protein sequences
2 Non-resistant protein sequences
After preprocessing, the sequences were:
* Labeled as resistant (1) or non-resistant (0)
* Merged into a single FASTA file
* Randomly shuffled
* Split into training (80%) and testing (20%) datasets using stratified sampling


# Methodology
The workflow of this project consists of the following steps:
1. Data collection from the PATRIC database
2. Data preprocessing and sequence labeling
3. Feature extraction using the pretrained ProtBERT model
4. Global Average Pooling to generate fixed-length protein embeddings
5. Training a Random Forest classifier
6. Performance evaluation using:
   * Accuracy
   * Precision
   * Recall
   * F1-score
   * Confusion Matrix
   * ROC Curve
   * Area Under the Curve (AUC)
7. Feature importance analysis
8. Virtual mutation analysis

# Technologies Used
* Python
* Google Colab
* PyTorch
* Hugging Face Transformers
* ProtBERT (Rostlab/prot_bert)
* Scikit-learn
* Biopython
* NumPy
* Pandas
* Matplotlib

# Repository Contents
 Predicting_beta_lactam_resistance.ipynb
├── README.md
├── requirements.txt
├── train_data.fasta
├── test_data.fasta
├── ROC_CURVE ANALYSIS
├── Feature Importance.

# Model Evaluation
The Random Forest classifier was evaluated using:
* Classification Report
* Confusion Matrix
* ROC Curve
* ROC-AUC Score
* Five-fold Cross Validation
The project also includes feature importance analysis to identify influential ProtBERT embedding dimensions.


# Virtual Mutation Analysis
Virtual mutation analysis was performed by introducing amino acid substitutions into selected protein sequences and evaluating their effect on the predicted probability of beta-lactam resistance. This analysis demonstrates how sequence modifications can influence the model's resistance predictions.


# How to Run
1. Clone this repository.
git clone https://github.com/your-username/your-repository.git
2. Install the required Python packages.
pip install -r requirements.txt
3. Open the notebook in Google Colab or Jupyter Notebook.
4. Run all cells sequentially.


# Citation
If you use this repository in your research, please cite:
**Madiha Arshad.** *Predicting Beta-Lactam Resistance in Escherichia coli Using ProtBERT and Random Forest.* Final Year Project, Department of Bioinformatics.


# Author

**Madiha Arshad**
Bachelor of Science in Bioinformatics
Final Year Project

# License
This repository is intended for educational and research purposes.
