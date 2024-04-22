# Bayesian Network for Lymphography Data Analysis

## Overview
This repository contains code and data for analyzing lymphography data using Bayesian networks. The goal is to model the conditional dependencies between lymphography features and gain insights into the underlying relationships.

## Files

### 1. BayesianNetwork.ipynb
- Jupyter notebook containing the analysis.
- Explore the dataset, build a Bayesian network, and perform inference.
- Includes visualizations of the network structure.

### 2. Data
- **lymphography_data.csv**: Dataset with lymphography data.
- **lymphography_names.csv**: Descriptions of dataset features.

## Getting Started
1. Clone this repository to your local machine.
2. Install the necessary dependencies (e.g., Python, Jupyter Notebook).
3. Open `BayesianNetwork.ipynb` to run the analysis.

## Methodology

### Data Preprocessing
The code performs the following data preprocessing steps (details in the provided notebooks):
- Handling missing values
- Verifying data types
- Generating correlation plots to explore feature relationships
- Reducing the original four classes to two binary classes:
  - Class 0: Metastases
  - Class 1: Malign Lymph
- Converting remaining classes to binary (0 & 1)

### Feature Selection
The project employs the Chi-squared test (Chi2) to identify the most relevant features for classification.

### Model Building
1. Bayesian Network
   - Library: pgmpy
   - Estimators: Maximum Likelihood and Bayesian estimators are compared for model construction.
   - Structure Learning: The Hill Climbing Algorithm is used to estimate Conditional Probability Distributions (CPDs).
   - Model Selection: A balance is sought between model complexity and classification accuracy.
   
2. Artificial Neural Network (ANN)
   - Library: Keras
   - Activation Functions: Various activation functions are explored (relu, sigmoid, softmax, tanh) to find the most suitable option for the network.
   - Optimizers: Experiments are conducted with SGD and other optimizers to optimize learning.
   - Hyperparameter Tuning: Batch size and epochs are tuned to achieve optimal performance.

### Evaluation & Further Exploration
The project plans to:
- Evaluate both models using metrics like accuracy, precision, recall, etc.
- Investigate techniques for model interpretability, especially for the ANN.
- Consider potential improvements and further analysis.

## Dependencies
- pgmpy (for Bayesian Network)
- Keras (for ANN)
- Scikit-learn (potential for evaluation metrics)
- (List any other libraries used in your project)

## Contributions
Contributions are welcome! Feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
