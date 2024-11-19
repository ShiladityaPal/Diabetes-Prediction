# Diabetes Prediction with Machine Learning

This project implements a machine learning pipeline to predict diabetes based on the **Diabetes dataset**. It uses multiple classification models, evaluates their performance, and allows users to input data for real-time predictions.

## Features
- **Classification Models**:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - Support Vector Machine (SVM)
  - Gradient Boosting
- **Performance Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC-AUC
- **User Interaction**:
  - Accepts real-time user input to predict diabetes likelihood.
  - Outputs prediction probabilities from all models.

## Requirements
The following Python libraries are required:
- `pandas`
- `scikit-learn`
- `numpy` (optional but commonly required for `scikit-learn`)
- `warnings` (for suppressing warnings)

You can install them using:
```bash
pip install pandas scikit-learn numpy
```

## Dataset
The project uses the built-in **Diabetes dataset** from `sklearn.datasets`. The target variable is binarized based on the median value to enable binary classification.

## How It Works
1. **Data Preprocessing**:
   - Features are standardized using `StandardScaler`.
   - The target variable is binarized for classification.

2. **Model Training**:
   - Five different models are trained using the preprocessed data.
   - Tree-based models (e.g., Decision Tree, Random Forest, Gradient Boosting) use raw data.
   - Logistic Regression and SVM use scaled data.

3. **Model Evaluation**:
   - Performance metrics for each model are calculated and presented in a summary table.

4. **Interactive Prediction**:
   - Users input feature values.
   - The pipeline predicts diabetes likelihood using all trained models.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/diabetes-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd diabetes-prediction
   ```
3. Run the script:
   ```bash
   python diabetes_prediction.py
   ```
4. Follow on-screen prompts to input feature values for real-time prediction.

## Example Output
### Model Performance:
| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.85     | 0.82      | 0.87   | 0.84     | 0.90    |
| Decision Tree       | 0.80     | 0.75      | 0.79   | 0.77     | 0.82    |
| Random Forest       | 0.88     | 0.86      | 0.89   | 0.87     | 0.92    |
| SVM                 | 0.87     | 0.83      | 0.88   | 0.85     | 0.91    |
| Gradient Boosting   | 0.89     | 0.87      | 0.90   | 0.88     | 0.93    |

### Prediction Results:
After entering feature values, the output looks like:
```
Chances of having diabetes (by model):
Logistic Regression: 0.75
Decision Tree: 0.81
Random Forest: 0.89
SVM: 0.78
Gradient Boosting: 0.92
```

## Contributing
Feel free to open issues or submit pull requests if you'd like to contribute. Suggestions and improvements are welcome!
