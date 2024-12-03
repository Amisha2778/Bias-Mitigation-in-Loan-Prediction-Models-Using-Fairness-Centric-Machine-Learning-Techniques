# Bias Mitigation in Loan Prediction Models Using Fairness-Centric Machine Learning Techniques

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Data and Preprocessing](#data-and-preprocessing)
- [Methodology](#methodology)
- [Results](#results)
- [How to Run](#how-to-run)
- [Future Work](#future-work)
- [Contributors](#contributors)

---

## Introduction
This project aims to address bias in loan prediction models by applying fairness-centric machine learning techniques. By employing the Disparate Impact Remover (DIR) and Fairlearn's Correlation Remover (CR), we mitigate both outcome-level and feature-level biases. This ensures fairness across demographic groups while maintaining model performance.

---

## Features
- Preprocessing algorithms to identify and mitigate bias:
  - Disparate Impact Remover (DIR)
  - Fairlearn's Correlation Remover (CR)
- Comparative analysis of bias mitigation techniques.
- Comprehensive fairness evaluation using metrics like Disparate Impact, Equal Opportunity, and Accuracy.
- Modular pipeline for easy adaptation to different datasets.

---

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - Scikit-learn
  - Fairlearn
  - AIF360
  - Pandas
  - Matplotlib, Seaborn (for visualization)
- **Frameworks**: Jupyter Notebook for experimentation.

---

## Data and Preprocessing
The dataset used contains anonymized loan application data, including:
- Applicant demographic information (e.g., gender, age).
- Financial attributes (e.g., income, loan amount).
- Loan approval status (target variable).

### Preprocessing Steps:
1. Handle missing values.
2. Normalize numerical features and encode categorical variables.
3. Identify sensitive attributes (e.g., gender) for fairness evaluation.

---

## Methodology
The project employs two fairness algorithms:
1. **Disparate Impact Remover (DIR)**:
   - Repairs the dataset by adjusting feature distributions to ensure outcome fairness.
   - Implemented using the AIF360 library.

2. **Fairlearn's Correlation Remover (CR)**:
   - Adjusts feature representations to remove correlations with sensitive attributes.
   - Ensures feature-level fairness during preprocessing.

### Combination Model:
The DIR and CR algorithms are combined to create a robust framework that addresses both outcome-level and feature-level biases.

---

## Results
The results demonstrate the effectiveness of the fairness algorithms:
- **Metrics**:
  - Improved fairness scores (e.g., Disparate Impact).
  - Maintained high predictive accuracy with minimal trade-offs.
- **Visualization**:
  - Receiver Operating Characteristic (ROC) curves.
  - Scatter plots for accuracy vs. disparity impact.
  - Metrics heatmap and radar chart.

| **Metric**               | **Original Model** | **DIR Only** | **CR Only** | **Combination** |
|--------------------------|--------------------|--------------|-------------|-----------------|
| **Accuracy**             | 81.2%             | 80.5%        | 81.0%       | 80.8%           |
| **Disparate Impact**     | 0.66              | 0.83         | 0.71        | 0.87            |
| **Equal Opportunity**    | Low               | Moderate     | Moderate    | High            |

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/loan-bias-mitigation.git
