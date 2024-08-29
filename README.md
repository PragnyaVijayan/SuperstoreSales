# Advanced Predictive Analytics for Forecasting Superstore Sales

**Authors:**
- **Pragnya Vijayan**
- **Vignesh Senthilkumar**

## Project Overview
This project focuses on building predictive models to forecast **sales** and **profit** for a large Superstore chain. The dataset used for this analysis was sourced from Kaggle (originally from Tableau), and the project aims to provide insights into which factors most strongly influence product sales and profits.

## Objective
The goal is to understand the key features that drive sales and profits and to build robust regression models to predict these values. Insights from this analysis can guide the Superstore in targeting customer segments, geographical regions, and product categories to optimize performance.

## Key Steps in the Project:
1. **Data Visualization**:
   - Sales and profit distributions were visualized to understand the general trends and identify potential outliers.
   - A time series analysis was conducted to observe trends over 6-month intervals from 2014 to 2018.

2. **Correlation Analysis**:
   - Features such as Category, Sub-category, Postal Code, and City were found to have varying degrees of correlation with sales and profit.
   - The results of the analysis informed feature importance ranking in the model training phase.

3. **Modeling**:
   - Five different models were tested:
     - **Linear Regression**
     - **Decision Tree**
     - **Random Forest**
     - **XGBoost**
     - **Dense Neural Network**
   - A train-test split was applied, and data normalization was done using **StandardScaler**.

4. **Model Selection**:
   - **Random Forest** was identified as the best model for predicting **Profit**.
   - **XGBoost** was found to be the most suitable model for **Sales** predictions.
   - **Linear Regression** did not perform well, while **Neural Networks** were competitive for some models but underperformed compared to the Random Forest and XGBoost.

5. **Feature Importance**:
   - Feature importance analysis revealed that **Postal Code**, **Sub-Category**, **Quantity**, and **City** were the most influential features in both Sales and Profit models.

## Conclusions:
- The Superstore should focus on geographical targeting (via Postal Code and City) and product analysis (via Sub-Category and Quantity) to enhance sales and profits.
- **Overfitting** was observed in the **Random Forest** model, particularly for sales prediction. The testing score was lower than the training score, indicating that the model fit too closely to the training data.
- **Corrective Measures**: Techniques such as **hyperparameter tuning**, **regularization**, and using a **simpler model** can help reduce overfitting. Additionally, **cross-validation** could provide more reliable estimates of model performance.
- While high correlation with the target variable helps, it is not the sole determinant of a feature’s importance in model predictions.

## Technologies Used:
- **Python**
- **Pandas**
- **Scikit-learn**
- **XGBoost**
- **TensorFlow** (for Neural Networks)
- **Data visualization libraries**: Matplotlib, Seaborn
- **StandardScaler** for normalization

## How to Run:
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Run the model training script:
   ```bash
   python csci_184_copy.py

## Future Work:
- Improving Accuracy: Hyperparameter tuning should be applied to the XGBoost and Random Forest models to further minimize testing error and enhance model generalization.
- Addressing Overfitting: Implement techniques like dropout for Neural Networks, regularization methods (e.g., L2 regularization), and early stopping to prevent overfitting in both - Random Forest and Neural Network models.
- Model deployment for real-time sales and profit predictions.
- Investigating other machine learning models like LightGBM or CatBoost, which may provide better accuracy and lower overfitting.
- Use of cross-validation for more reliable error estimation across different model splits.

## Project Report
[Click here to read more about the project](https://drive.google.com/file/d/1waL1cD73AOBGn2YLaOabVI5kmqjZMLw6/view?usp=sharing)
