# Titanic Machine Learning Project: Final Report

## Objective
The objective of this project is to analyze and predict passenger survival during the Titanic disaster using machine learning models. This project demonstrates the complete ML pipeline, including data preprocessing, feature engineering, model evaluation, and optimization.

## Dataset
The Titanic dataset consists of features like:
- **Survival**: Target variable (0 = No, 1 = Yes)
- **Pclass**: Passenger class (1st, 2nd, 3rd)
- **Sex**: Gender of the passenger
- **Age**: Age of the passenger
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Fare**: Ticket fare
- **Embarked**: Port of embarkation (C, Q, S)


### 1. Data Exploration and Visualization
- **Techniques**:
  - Summary statistics to understand central tendencies and variability.
  - Bar plots and histograms for visualizing survival trends across gender, age, and class.
- **Findings**:
  - Women had higher survival rates compared to men.
  ![gender survival](<Images/women survival.png>)

  - 1st class passengers were more likely to survive than those in 2nd or 3rd class.
  ![1st class](Images/tickets.png)

  - Queenstown passengers had a higher survival rate compared to those from Cherbourg or Southampton.
  ![embarked](Images/embarked.png)

  - Southampton was a key embarkation point for passengers, particularly those in the lower ticket classes.
  - Cherbourg attracted wealthier passengers in 1st class.
  - Queenstown primarily catered to 3rd-class passengers, indicating economic or geographic trends among the boarding points.

  ![ticketembark](<Images/ticket by embark.png>)

  - Passengers with lower family on board had the higher survival rate.
  ![siblings](Images/siblings.png)

  ![parents](Images/parents.png)

### 2. Data Cleaning and Preprocessing
- **Steps Taken**:
  - Imputed missing values for `Age` using median values grouped by `Pclass` and `Sex`.
  - Filled missing `Embarked` values with the most frequent category.
  - Scaled numerical features like `Age` and `Fare` for uniformity.

### 3. Feature Engineering
- **Features Created**:
  - `FamilySize`: Sum of `SibSp` and `Parch`.
  - `IsAlone`: Binary feature indicating whether the passenger was traveling alone.
- **Feature Selection**:
  - Retained features with high correlation to survival or importance from model analysis.

### 4. Model Training and Evaluation
- **Models Used**:
  - Logistic Regression
  - Random Forest
  - Support Vector Machine
- **Metrics**:
  - Accuracy
  - Precision, Recall, and F1-Score
  - ROC-AUC for classification quality
- **Results**:
  Random Forest consistently outperformed other models in all metrics.

### 5. Model Optimization
- **Hyperparameter Tuning**:
  - GridSearchCV was used  to find the best model.
  - The optimized model Decision achieved an accuracy of 81%.

### 6. Testing and Submission
- **Prediction**:
  - Final model was applied to the test dataset.
  - Results were saved in a submission file format.



## Conclusion
The project demonstrated a comprehensive approach to machine learning, with Decision Tree emerging as the best model. Future work could explore deep learning or external data sources for further enhancement.

## Recommendations
- Use ensemble methods like Gradient Boosting.
- Include text analysis for features like names and tickets.
- Explore imputation methods like KNN for handling missing data.

## Appendix
- **Code**: Attached in the Jupyter Notebook.
- **Visualizations**: Included in the notebook for better understanding of trends.

