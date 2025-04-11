# 💊 An End-to-End Pipeline for Drug-Likeness Evaluation

Welcome to **"An End-to-End Pipeline for Drug-Likeness Evaluation"**, a fully integrated project that bridges the gap between cheminformatics and modern machine learning. This repository provides a complete workflow to classify molecules as *drug-like* or *non-drug-like* using both traditional machine learning models and cutting-edge transformer-based deep learning approaches like ChemBERTa.

---

## 🚀 What This Project Does
This pipeline builds a binary classification system to determine the drug-likeness of molecules. We start with raw molecular data and end with a well-evaluated predictive model—comparing the strengths of Random Forests and ChemBERTa.

### Core Steps:
- ✅ Automated dataset collection from **ChEMBL API**
- 🧪 Feature engineering using **RDKit** for molecular descriptors
- 🎯 Traditional ML with **Random Forest Classifier**
- 🤖 Advanced deep learning with **ChemBERTa**, a transformer model built for molecular SMILES
- 📊 In-depth evaluation with rich visualizations

---

## 📁 Project Structure
```
├── druglikeness_dataset_final.csv     # Cleaned dataset with extracted features
├── non_druglike_labeled.csv          # Negative samples from ChEMBL
├── chemberta_finetuned/              # Output folder for ChemBERTa fine-tuning
├── logs/                             # Training logs from Hugging Face Trainer
├── images/                           # Plots: PCA, ROC, correlation heatmaps, etc.
├── chemistry.ipynb                   # Main Jupyter notebook with all code
├── model_comparison.png              # Side-by-side visual comparison of models
```

---

## 🔬 Breakdown of Major Components

### 1. 📊 Exploratory Data Analysis (EDA)
We explore the structure and relationships in the molecular data:
- Histograms for feature distribution
- Heatmap for feature correlations
- Principal Component Analysis (PCA) to visualize dimensionality

### 2. ⚙️ Traditional ML with Random Forest
We extract numerical molecular features with RDKit and train a Random Forest classifier:
- Feature importance insights
- Fast training, good baseline performance
- Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC

### 3. 🤯 Transformer-Based Deep Learning with ChemBERTa
We tokenize SMILES strings and fine-tune **ChemBERTa** from Hugging Face:
- Utilizes `AutoTokenizer` and `AutoModelForSequenceClassification`
- Handles raw SMILES directly, no manual feature engineering needed
- Trained using Hugging Face’s `Trainer` API
- Logged with W&B (optional)

### 4. 🧪 Evaluation & Comparison
We assess both models using:
- Confusion matrices
- ROC curves
- Classification reports
- **Bar chart comparison** of Accuracy, Precision, Recall, F1, and ROC-AUC

---

## 🛠️ Installation & Requirements
Install all dependencies from `requirements.txt`:
```bash
pip install -r requirements.txt
```
### Required Packages:
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`
- `rdkit`
- `transformers`, `datasets`
- `wandb` *(optional, for training logs)*

---

## 💾 Model Exporting
We save trained models for future use:
- 🧠 Random Forest: `rf_model.pkl` (via `joblib`)
- 🤖 ChemBERTa: Automatically saved under `./chemberta_finetuned/`

---

## 📤 Output Artifacts
- 🔍 Pickled traditional model
- 🧠 Fine-tuned ChemBERTa model
- 📈 Metrics printed and visualized
- 📊 Comparison charts and performance plots

---

## 🌟 Highlights
- Seamless integration of traditional and transformer-based modeling
- Modular design for easy adaptation to other molecular tasks
- Comprehensive visuals to aid interpretation

---

## 🔭 Future Enhancements
- Support for regression (e.g., Lipinski score, logP)
- Integrate MolBERT, SMILES-BERT, or other DL models
- Expansion to multi-class classification or ADMET properties

---

## 👤 Author
Developed by [Your Name] — passionate about drug discovery, data science, and AI. Feel free to fork, star ⭐, and contribute!

---

## 📜 License
This project is licensed under the **MIT License** — open for use and collaboration.

