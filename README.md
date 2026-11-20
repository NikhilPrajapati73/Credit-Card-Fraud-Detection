# Credit Card Fraud Detection & Predictive Risk Analysis

A CA-ready Jupyter Notebook project using the supplied credit-card transaction dataset.

## Folder structure

```text
Credit Card Fraud Detection/
├── data/
│   ├── creditcard.csv              
│   └── creditcard_clean.csv        
├── notebooks/
│   └── Analysis.ipynb
├── models/                         
├── outputs/                        
├── requirements.txt
└── README.md
```

## 1. Put the datasets in place

Copy your two CSV files into the `data` folder. The notebook uses `creditcard.csv` as the primary source and optionally compares `creditcard_clean.csv`.

The datasets are not bundled in this ZIP because they are large. Use the files supplied separately.

## 2. Install Python packages

Open Command Prompt or PowerShell in this project folder:

```bash
python -m venv .venv
.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

If you use Anaconda, you can install the same requirements into your environment.

## 3. Start Jupyter

```bash
jupyter notebook
```

Open `notebooks/Analysis.ipynb` and run cells from top to bottom.

## 4. Important methodology

- The original dataset is the primary source.
- The cleaned dataset is only used for a comparison; its `Time` and `Amount` columns are already scaled.
- The notebook uses stratified train/validation/test splits.
- Model selection and threshold selection use validation data only.
- Final metrics are calculated once on the held-out test set.
- Accuracy is not treated as the primary metric because fraud is highly imbalanced.
- The project reports precision, recall, F1, ROC-AUC, PR-AUC and confusion matrix.

## 5. Project originality

Use the friend's repository only as a reference for broad project organization. Keep your own notebook, analysis, charts, model experiments, results, report and explanations. Do not submit another person's notebook or claim their work as yours.

## 6. Limitations

The `V1`–`V28` fields are anonymized features. The dataset is historical and anonymized. A fraud prediction is a review signal, not proof of fraud or an automated banking decision.
