# 🧪 An-End-to-End-Pipeline-for-Drug-Likeness-Evaluation  

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)  
![RDKit](https://img.shields.io/badge/RDKit-Cheminformatics-orange?logo=flask&logoColor=white)  
![PyTorch](https://img.shields.io/badge/PyTorch-ML-red?logo=pytorch&logoColor=white)  
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)  

> ⚗️ **A Python-based pipeline for drug-likeness evaluation** using cheminformatics, molecular descriptors, and machine learning.  
> This project automates the journey from **raw compound SMILES → featurization → ADMET/drug-likeness scoring → structured report export**.  

---

## 📌 Table of Contents  

- ✨ [Features](#-features)  
- 📦 [Installation](#-installation)  
- ⚡ [Usage](#-usage)  
- 🔄 [Pipeline Workflow](#-pipeline-workflow)  
- 💻 [Tech Stack](#-tech-stack)  
- 🤝 [Contributing](#-contributing)  
- 📜 [License](#-license)  
- 👩‍💻 [Author](#-author)  

---

## ✨ Features  

- 🧬 **Featurization** with RDKit (molecular descriptors, fingerprints)  
- 📏 **Rule-based scoring** (Lipinski’s Rule of Five, LogP, HBD/HBA counts, etc.)  
- 🤖 **Machine Learning models** integrated: Random Forest & ChemBERTa  
- 📂 **Batch processing** of molecules (CSV / SMILES input)  
- 📊 **Exportable reports** in JSON / CSV formats  
- 🔧 **Modular & Extensible** – add your own metrics or models  

---

## 📦 Installation  

Clone this repository and install the dependencies:  

```bash
git clone https://github.com/rutujapatil-afk/An-End-to-End-Pipeline-for-Drug-Likeness-Evaluation.git
cd An-End-to-End-Pipeline-for-Drug-Likeness-Evaluation
pip install -r requirements.txt
⚡ Usage
🖥️ Command Line
bash
Copy code
python evaluate.py \
  --input compounds.smi \
  --output report.json \
  --metrics lipinski,logp,vdw
🐍 Python API
python
Copy code
from pipeline import DrugLikenessEvaluator

# Initialize evaluator
evaluator = DrugLikenessEvaluator()

# Evaluate a compound (Aspirin SMILES)
report = evaluator.evaluate("CC(=O)Oc1ccccc1C(=O)O")

print(report)
💡 Sample Output (JSON):

json
Copy code
{
  "compound": "Aspirin",
  "Lipinski": true,
  "logP": 1.19,
  "MW": 180.16,
  "HBD": 1,
  "HBA": 4,
  "Verdict": "Drug-like"
}
🔄 Pipeline Workflow
text
Copy code
[ Input SMILES/CSV ] 
        ↓
[ Featurization 🔬 (RDKit) ] 
        ↓
[ ML Models 🤖 (Random Forest, ChemBERTa) ] 
        ↓
[ Drug-likeness Metrics 📏 & ADMET Rules ] 
        ↓
[ JSON/CSV Report Export 📊 ]
💻 Tech Stack
Category	Tools / Libraries
Language	🐍 Python 3.8+
Cheminformatics	🧪 RDKit
Machine Learning	🔥 PyTorch • 🤖 scikit-learn
Data Handling	📊 pandas • NumPy
Visualization	📈 Matplotlib • Seaborn
Version Control	🗂️ Git • GitHub

🤝 Contributing
Pull requests are welcome! 🚀
For major changes, please open an issue first to discuss what you’d like to change.
Make sure to update tests where appropriate ✅.

📜 License
This project is licensed under the MIT License.

👩‍💻 Author
Rutuja Patil
🔗 GitHub • 💼 LinkedIn
