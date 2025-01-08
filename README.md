# Predicting Vaccine Responses for H1N1 and Seasonal Flu

## Project Overview
This project explores three machine learning methods (Decision Tree, XGBoost, and Neural Network) to predict vaccine responses for H1N1 and seasonal flu. The models were evaluated on performance metrics such as precision, recall, F1-score, and accuracy.

## Dataset
The dataset includes features related to demographic, health conditions, and vaccine responses. The target variables are:
- **H1N1 vaccine response**
- **Seasonal flu vaccine response**

Key preprocessing steps:
- Handling missing values.
- Encoding categorical variables.
- Normalizing data for neural networks.

## Methodologies
### 1. Decision Tree
- **Purpose**: Baseline model to understand the data.
- **Strengths**: Fast and interpretable.
- **Limitations**: Struggles with complex data or imbalanced classes.

### 2. XGBoost
- **Purpose**: Ensemble method to improve prediction accuracy.
- **Strengths**: Excellent performance on complex datasets, handles missing values effectively.
- **Limitations**: Higher computational cost, requires extensive hyperparameter tuning.

### 3. Neural Network
- **Purpose**: Leverage multi-layer perceptrons to model nonlinear relationships.
- **Strengths**: Learns complex patterns and performs well on larger datasets.
- **Limitations**: Requires more data, computationally expensive, and sensitive to hyperparameter choices.

## Results
### Performance Metrics (H1N1)
| Model            | Precision (0/1) | Recall (0/1) | F1-Score (0/1) | Accuracy |
|-------------------|-----------------|--------------|----------------|----------|
| Decision Tree     | 0.79 / 0.55    | 0.85 / 0.46 | 0.82 / 0.50    | 0.80     |
| XGBoost           | 0.87 / 0.69    | 0.94 / 0.48 | 0.91 / 0.57    | 0.84     |
| Neural Network    | 0.86 / 0.65    | 0.90 / 0.50 | 0.88 / 0.56    | 0.83     |

### Key Observations:
- Decision Tree performed well on basic classification but struggled with minority class (label 1).
- XGBoost outperformed others in all key metrics, demonstrating strong generalization.
- Neural Network showed competitive results but required more data and computation compared to XGBoost.

## Lessons Learned
1. **Model Selection**:
   - Decision Tree is suitable for quick prototypes.
   - XGBoost is ideal for structured data and imbalanced datasets.
   - Neural Networks excel with large, complex datasets but demand careful tuning.
2. **Preprocessing**:
   - Neural Networks benefit significantly from feature normalization.
   - Imbalanced datasets require techniques like resampling or class-weight adjustments.
3. **Performance Trade-offs**:
   - While XGBoost provided the best balance of accuracy and computational efficiency, Neural Networks could potentially surpass with additional data.

## How to Use
### 1. Prerequisites
- Python 3.8+
- Required libraries: `xgboost`, `sklearn`, `tensorflow`, `pandas`, `numpy`


