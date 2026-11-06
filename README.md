# 🏥 Hospital Readmission Risk Prediction Using Deep Learning

### Predicting 30-Day Hospital Readmission Risk Using a Multi-Layer Perceptron (MLP)

## 📌 Project Overview

Hospital Readmission Risk Prediction is a healthcare-focused Machine Learning and Deep Learning project designed to identify patients who are likely to be readmitted to a hospital within 30 days after discharge.

Unplanned hospital readmissions increase healthcare costs, occupy limited hospital resources, and may indicate gaps in discharge planning or post-discharge patient care.

This project uses the **Diabetes 130-US Hospitals Dataset (1999–2008)** to develop a predictive model using a **Multi-Layer Perceptron (MLP)** with TensorFlow and Keras.

The model analyzes patient demographics, medical history, hospital encounters, medication information, and previous hospital visits to estimate readmission probability.

The ultimate objective is to help hospitals identify high-risk patients and prioritize follow-up care.

## 🎯 Business Objectives

- Predict whether a patient will be readmitted within 30 days.
- Identify important factors associated with hospital readmissions.
- Develop a Deep Learning model using an MLP architecture.
- Handle missing values and imbalanced target classes.
- Evaluate model performance using multiple classification metrics.
- Perform structured error analysis to understand false positives and false negatives.
- Generate patient-level risk scores to support healthcare follow-up planning.

## 📊 Dataset Information

**Dataset:** Diabetes 130-US Hospitals Dataset

**Source:** UCI Machine Learning Repository

- Total patient encounters: 101,766
- Original dataset columns: 50
- Historical period: 1999–2008
- Target variable: `readmitted`

### Target Classification

| Original Value | Classification | Meaning |
|---|---|---|
| `<30` | 1 | Readmitted within 30 days |
| `>30` | 0 | Readmitted after 30 days |
| `NO` | 0 | Not readmitted |

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Manipulation | Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Deep Learning | TensorFlow, Keras |
| Model Architecture | Multi-Layer Perceptron (MLP) |
| Development Environment | Jupyter Notebook |

## ⚙️ Project Workflow

1. **Business Understanding:** Define the hospital readmission problem and identify business objectives.

2. **Data Understanding:** Explore the dataset, understand patient attributes, and analyze the target variable.

3. **Data Preprocessing:** Handle missing values, clean invalid records, encode categorical variables, and scale numerical features.

4. **Feature Engineering:** Prepare meaningful patient and hospital encounter features.

5. **Data Splitting:** Use patient-level splitting to reduce data leakage between training, validation, and test sets.

6. **Model Development:** Build an MLP neural network using TensorFlow/Keras.

7. **Model Training:** Train the model using the Adam optimizer and Binary Cross-Entropy loss, with class weighting to address class imbalance.

8. **Model Evaluation:** Evaluate performance using Accuracy, Precision, Recall, F1-Score, ROC-AUC, PR-AUC, and Confusion Matrix.

9. **Error Analysis:** Analyze false positives and false negatives to understand prediction errors.

10. **Business Insights:** Generate patient-level predictions and categorize patients into Low, Medium, and High readmission-risk groups.

## 🧠 Deep Learning Architecture

The project uses a **Multi-Layer Perceptron (MLP)**, a feedforward neural network suitable for structured/tabular data.

### Architecture Components

- Input Layer: Receives preprocessed patient features.
- Hidden Layers: Dense layers with ReLU activation.
- Output Layer: Single neuron with Sigmoid activation.
- Optimizer: Adam.
- Loss Function: Binary Cross-Entropy.

The Sigmoid output produces a probability between 0 and 1, representing the predicted likelihood of readmission.

## 📈 Model Evaluation and Results

The model is evaluated using a held-out test dataset containing 14,050 patient encounters.

| Evaluation Metric | MLP Result |
|---|---:|
| ROC-AUC | 0.656 |
| PR-AUC | 0.196 |
| Recall | 59% |
| Precision | 17% |
| Accuracy | 63% |

### Key Findings

- The MLP achieved a ROC-AUC of 0.656.
- The model identified approximately 59% of actual 30-day readmissions at the selected operating threshold.
- The High-Risk patient group showed a 24.1% readmission rate, approximately 2.2 times the overall average.
- Previous inpatient visits and discharge-related features were among the strongest model risk-score drivers.
- Class weighting helped address the imbalance between readmitted and non-readmitted patients.

**Note:** These results represent an educational model evaluation, not a clinically validated prediction system.

## 📁 Repository Structure

```text
Hospital-Readmission-Risk-Prediction/
│
├── Hospital_Readmission_MLP.ipynb
│
├── Hospital_Readmission_Vigneshbabu.ipynb
│
├── Hospital_Readmission_Project_Explanation.docx
│
├── MLP_Hospital_Readmission_Assignment.docx
│
├── diabetic_data.csv
│
├── IDS_mapping.csv
│
├── readmission_predictions_test.csv
│
└── README.md
```

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Vigneshbabu4/Hospital-Readmission-Risk-Prediction-.git
```

### 2. Navigate to the Project Directory

```bash
cd Hospital-Readmission-Risk-Prediction-
```

### 3. Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Execute the Notebook

Open `Hospital_Readmission_MLP.ipynb` and execute the cells sequentially to explore data preprocessing, model development, training, evaluation, and predictions.

## 💡 Real-World Applications

- Identifying patients who may require additional post-discharge monitoring.
- Prioritizing follow-up appointments.
- Supporting hospital resource planning.
- Improving discharge planning strategies.
- Helping healthcare teams allocate follow-up resources more effectively.

## 🔮 Future Enhancements

- Experiment with advanced architectures for tabular data.
- Improve prediction performance through feature engineering and hyperparameter tuning.
- Integrate explainable AI techniques such as SHAP.
- Develop an interactive dashboard for patient-risk monitoring.
- Build a web-based application for healthcare professionals.
- Validate the model using more recent and diverse healthcare datasets.

## ⚠️ Disclaimer

This project is developed for educational, research, and machine learning experimentation purposes. The dataset is historical, covering 1999–2008. Predictions should not be used as a substitute for professional medical judgment or clinical decision-making.

## 👨‍💻 Author

**Vignesh Babu Guthi**

B.Tech – Computer Science and Engineering (AI & ML)

GitHub: [@Vigneshbabu4](https://github.com/Vigneshbabu4)

---

⭐ If you find this project interesting, consider giving the repository a star!

**Built with Python, Machine Learning, and Deep Learning.**
