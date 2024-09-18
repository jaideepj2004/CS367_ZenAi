# CS367_ZenAi

# Bayesian Network Classification

## Objective
Classify instances from a dataset into different classes using a Bayesian Network model. The dataset includes a target variable (`class`) and several features (`feature1` to `feature5`).

## Dataset
- **Format**: CSV file (`train.csv`)
- **Columns**:
  - `class` (Target Variable)
  - `feature1`, `feature2`, `feature3`, `feature4`, `feature5` (Independent Variables)

## Approach

### Data Preparation
1. **Loading the Data**:
   - The dataset is read using `pandas`, with columns explicitly named for clarity.
2. **Separating Features and Target**:
   - Independent variables (`feature1` to `feature5`) are separated from the target variable (`class`).

### Bayesian Network Model
1. **Model Definition**:
   - A Bayesian Network structure is defined where each feature influences the class. Each feature directly affects the class variable.
2. **Training**:
   - The model is trained using `MaximumLikelihoodEstimator` to estimate conditional probabilities from the data.
3. **Inference**:
   - `Variable Elimination` is used for querying the network. Predictions are made based on observed feature values.

### Predictions and Evaluation
1. **Query Example**:
   - For given feature values `[107, 10.1, 2.2, 0.9, 2.7]`, the network predicts the probability distribution over possible classes.

## Usage

1. **Run the Model**:
   - Ensure `train.csv` is available in the working directory.
   - Execute the script to train the Bayesian Network and perform predictions.

2. **Dependencies**:
   - `pandas`
   - `pgmpy`

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
