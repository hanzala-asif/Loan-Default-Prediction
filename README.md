# Loan-Default-Prediction

# Credit Risk Prediction

## Task Objective

The main aim of this assignment is to create a machine learning model that would indicate the likelihood of loan applicant defaulting on a loan. The prediction is important in limiting risks faced by financial institutions in making effective decisions on loan approvals.

## Your Approach

1.  Initial Inspection and Data Loading: The initial inspection of the dataset of loan default and loading was done through pandas using the Loan default.csv file. The first step was to conduct an inspection and check whether any values were missing and the type of data and the column information.
2.  Data Cleaning and Preparation Data Cleaning Data data were further cleaned by removing the column of LoanID because it is not predictive. A label encoder was used to transform categorical features into numerical forms. The dataset was further divided into training and testing (80/20 split) and each of the features was scaled with the help of the StandardScaler to guarantee the best model performance.
3.  Exploration data Analysis (EDA): A range of visualizations was created to get to know the dataset more:
    *   Distribution of Loan Amount: A Histogram was used to demonstrate the distribution of loan amounts.
    *   Loan Default vs. Education Level: A count plot was used to demonstrate the relationship between loan default status and education levels.
    *   Distribution of Income A histogram was used to show the distribution of incomes of the applicants.
    *   Correlation Heatmap**: The correlation between the numerical features was represented in a heatmap, where possible relationship with the target variable was determined.
4.  Model Training: The model that was selected to perform binary classification is the Logistic Regression model since this model is interpretable and it can be effectively used to perform binary classification. The scaled training data were trained on the model.
5.  Model Evaluation: The performance of the trained model was evaluated with:
    *   Accuracy Score: The total correctness of the predictions of the model.
    *   Confusion Matrix: This is a comprehensive list of the true positives, true negatives, false positives, and false negatives.
    *   Classification Report**: Gave precision, recall, and f1-score per class.

## Results and Insights

### Key Findings from EDA:

* The data set has 255 347 records and 18 variables where there are no empty values in all features.
The target variable, which is the default, has a severe case of class imbalance with around 88.4 of the applicants not defaulting (class 0) and 11.6 of the applicant defaulting (class 1).
*   Figures of the variables of LoanAmount, Education, and Income offered information about their distributions and connection to loan default.

The regression model produces a linear relationship between the dependent and independent variables of the model.<|human|>Model Performance (Logistic Regression): The model represents a linear relationship between the independent and dependent variable of the model.

*   Accuracy: 0.8851 (approximately 88.51%)
*   Confusion Matrix:

    Predicted No Default Predicted Default
    | :---------- | :------------------- | :---------------- |
    | Actual No Default | 45020                | 119               |
    | Actual Default    | 5751                 | 180               |

*   **Classification Report**:

    ```
                  precision recall f1-score support

               0       0.89      1.00      0.94     45139
               1       0.60      0.03      0.06      5931

        accuracy                           0.89     51070
       macro avg       0.74      0.51      0.50     51070
    weighted avg       0.85      0.89      0.84     51070
    ```

The Model Evaluation has provided an insight into the model's strengths and weaknesses as follows:

* The model demonstrated a good overall accuracy, which was mostly because of the high accuracy in prediction of the majority class (non-defaulters).
*   But the recall of the **Default or the class 1 class is very low (0.03) which means that this model is not good at predicting correctly the defaulting applicants. This is the problem that is usual with unbalanced datasets.
The class 1 accuracy is 0.60 which indicates that the model is accurate 60 percent of the time when default is predicted.

### Future Work:

*   Reduce the problem of class imbalance with methods like SMOTE (Synthetic Minority Over-sampling Technique) or by changing the weights of classes during training of the model.
*   Try more recent classification methods such as the Random Forest, Gradient Boosting, or XGBoost, which are typically more resistant to an imbalanced dataset and can do more complex correlation modeling.
*   Hyperparameter tuning to maximize the performance of the selected model.
*   Investigate feature engineering to generate new more informative features using existing features.

## Files Included:

Paper/Folder: credit risk prediction The folder of the analysis, EDA, model training and evaluation is in the Jupyter Notebook.
*   `Loan_default.csv`: The dataset used for this task.
*   `plots/`: Directory containing generated plots from EDA and model evaluation.
