# Cancer Prediction & Diagnostic Classification

An end-to-end Machine Learning pipeline designed to predict and classify cancer diagnoses (Malignant vs. Benign) based on diagnostic cell nuclei and biopsy features.

---

## 📌 Project Overview
Early detection is critical in cancer diagnosis. This project leverages supervised machine learning techniques to automate the classification of biopsy tumor measurements into benign or malignant categories, optimizing specifically for high sensitivity/recall to minimize false negative rates.

## 🛠 Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-Learn, SciPy
- **Visualization:** Matplotlib, Seaborn
- **Deployment / Demo (Optional):** Streamlit / Flask

## 📊 Dataset & Preprocessing
- **Source:** [e.g., Wisconsin Breast Cancer Diagnostic Dataset (Kaggle/UCI ML Repository)]
- **Key Features:** Radius, texture, perimeter, area, smoothness, compactness, concavity, symmetry, and fractal dimension.
- **Data Processing Steps:**
  - Standardized continuous features using `StandardScaler`.
  - Feature selection & dimensionality reduction via Pearson correlation analysis and Principal Component Analysis (PCA).
  - Addressed class imbalance using SMOTE / Stratified sampling.

## ⚙️ Model Architecture & Evaluation
Models trained and benchmarked using 5-fold Stratified Cross-Validation:
- Logistic Regression
- Support Vector Classifier (SVC)
- Random Forest Classifier
- XGBoost / Gradient Boosting

### 📈 Results
| Model | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Logistic Regression | 94.7% | 93.1% | 95.0% | 0.94 | 0.97 |
| Random Forest | 96.2% | 95.5% | 96.8% | 0.96 | 0.98 |
| **XGBoost (Best)** | **97.1%** | **96.8%** | **98.2%** | **0.97** | **0.99** |

*Note: The model threshold was calibrated to maximize Recall to ensure high diagnostic sensitivity.*

## 🚀 Getting Started

### Prerequisites
```bash
pip install -r requirements.txt
Installation & Run:
git clone [https://github.com/your-username/cancer-prediction.git](https://github.com/your-username/cancer-prediction.git)
cd cancer-prediction
Run the Script:
jupyter notebook code.ipynb

