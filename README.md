# YuvaIntern-Week5-Machine-Learning
Data Analytics Internship – Week 5 project focused on machine learning using Python and the Online Retail dataset. Includes data preprocessing, Random Forest Regression, hyperparameter tuning with RandomizedSearchCV, cross-validation, model evaluation using MAE, RMSE, and R², visualizations, and a detailed project report.


# YuvaIntern Week 5 – Machine Learning and Model Evaluation

## Project Overview

This project implements a Machine Learning workflow using Python and the Online Retail dataset. The main objective is to train a predictive model, optimize its hyperparameters, evaluate its performance, and document the findings.

A Random Forest Regressor is used to predict the quantity sold in the next recorded sales observation for a product.

## Objectives

- Prepare and preprocess retail transaction data.
- Create product-level daily sales features.
- Train a Random Forest Regression model.
- Tune hyperparameters using RandomizedSearchCV.
- Perform time-based cross-validation.
- Evaluate model performance using regression metrics.
- Visualize actual versus predicted values and feature importance.
- Document the workflow, results, limitations, and recommendations.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook in VS Code
- Microsoft Word

## Dataset

The project uses the Online Retail dataset, which contains transaction information such as:

- Invoice number
- Invoice date
- Product stock code
- Quantity
- Unit price
- Customer ID
- Product description

## Project Workflow

### 1. Data Preprocessing
- Loaded the dataset using Pandas.
- Converted date and numeric columns to appropriate data types.
- Removed rows with missing essential fields.
- Excluded non-positive quantities and unit prices for the sales analysis.
- Calculated revenue and prepared the working dataset.

### 2. Feature Engineering
Aggregated transactions by product and date to calculate:
- Daily quantity sold
- Average unit price
- Number of distinct transactions

The prediction target is the quantity in the next recorded sales observation for the same product.

### 3. Model Training
A Random Forest Regressor was trained using the selected input features. The data was sorted chronologically and split into training and testing sets.

### 4. Hyperparameter Tuning
RandomizedSearchCV was used to explore different combinations of:
- `n_estimators`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`

Three time-based cross-validation splits were used, with mean absolute error as the selection metric.

### 5. Model Evaluation
The model was evaluated using:

- **Mean Absolute Error (MAE):** Measures the average absolute prediction error.
- **Root Mean Squared Error (RMSE):** Penalizes larger prediction errors more heavily.
- **R-squared (R²):** Measures the proportion of target variation explained by the model.

### 6. Visualization
The project includes:
- Actual vs. Predicted Quantity scatter plot
- Random Forest Feature Importance chart
- Initial vs. Tuned Model Comparison

## Project Structure

```text
YuvaIntern-Week5-Machine-Learning/
├── Dataset/
├── Output/
│   ├── Model_Comparison.csv
│   ├── Final_Model_Predictions.csv
│   ├── Final_Model_Metrics.csv
│   └── YuvaIntern_Week5_Machine_Learning_Report.docx
├── Charts/
│   ├── Actual_vs_Predicted.png
│   └── Feature_Importance.png
├── Week5_Machine_Learning.ipynb
└── README.md
```

## Key Learning Outcomes

- Understanding the end-to-end Machine Learning workflow.
- Applying Random Forest Regression.
- Performing hyperparameter tuning and cross-validation.
- Evaluating predictive models using regression metrics.
- Creating visualizations to communicate model performance.
- Documenting model assumptions and limitations.

## Limitations

The target represents the next recorded sales observation, which may not correspond to the next calendar day. Days without recorded sales are not explicitly represented. The model also uses a limited set of features and should not be considered a production-ready demand forecasting system.

Future improvements could include creating a complete product-date calendar, incorporating zero-sales days, adding lagged sales and calendar features, comparing against a baseline model, and testing on a separate future period.

## Deliverables

- Python notebook containing the ML workflow
- Model comparison and prediction CSV files
- Final evaluation metrics
- Model evaluation visualizations
- Detailed Word report

## Internship Details

**Program:** YuvaIntern Data Analytics Internship  
**Task:** Week 5 – Implementing Machine Learning Algorithms and Model Evaluation  
**Dataset:** Online Retail

---

*This project was developed for educational purposes to practice machine learning, model evaluation, and data analytics.*
