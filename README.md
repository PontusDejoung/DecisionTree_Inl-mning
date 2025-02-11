# Wine Quality Prediction

## Project Description
This project uses a dataset containing the chemical properties of wines to predict wine quality. A decision tree model is employed, and hyperparameter tuning is performed to optimize performance.

## Data Description
The dataset used is from the file `WineQT.csv`, which contains 1,143 data points with 13 attributes:

- **fixed acidity**
- **volatile acidity**
- **citric acid**
- **residual sugar**
- **chlorides**
- **free sulfur dioxide**
- **total sulfur dioxide**
- **density**
- **pH**
- **sulphates**
- **alcohol**
- **quality** (Target variable, classification goal)
- **Id** (Removed from analysis)

## Modeling and Evaluation
### Data Handling
- The dataset is loaded and explored from the file `Pontus_DeJoung_decision_tree.ipynb`.
- The `Id` attribute is removed as it does not contribute to the predictive capability of the model.
- The dataset is split into training and test sets with an 80/20 distribution.

### Model Training
- A **Decision Tree Classifier** from `sklearn` is used.
- Grid Search is employed to optimize parameters:
  - `criterion`: gini, entropy
  - `max_depth`: None, 10, 50, 100, 150, 200
  - `min_samples_split`: 2, 10, 50
  - `min_samples_leaf`: 1, 5, 20, 30, 50

### Model Evaluation
- The best parameters are identified, and the model's accuracy is evaluated on both the training and test sets.

## Results
- A correlation matrix is generated to analyze relationships between attributes.
- A decision tree model is built and optimized using hyperparameter tuning.
- The model's precision and accuracy are evaluated on test data.
