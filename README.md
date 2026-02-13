# Employee Attrition Analysis

## Project Overview

This project focuses on analyzing employee attrition using a dataset containing various employee-related metrics. The goal is to identify key factors influencing whether employees leave the company and to build a predictive model to forecast attrition.

## Dataset

The dataset `HR_comma_sep 1.csv` contains information such as satisfaction level, last evaluation, number of projects, average monthly hours, time spent in the company, work accidents, promotions in the last 5 years, department, and salary, along with a target variable indicating whether an employee has 'left' the company.

## Exploratory Data Analysis (EDA) Key Findings

During the exploratory data analysis phase, several important insights were uncovered:

*   **Satisfaction Level**: Showed a strong negative correlation with employee attrition. Employees with lower satisfaction levels are significantly more likely to leave.
*   **Salary**: Employees with low salaries exhibited a higher attrition rate compared to those with medium or high salaries.
*   **Department**: Specific departments showed varying attrition rates, with some departments experiencing higher turnover than others.
*   **Duplicates and Missing Values**: The dataset was cleaned by dropping over 3000 duplicate entries.

## Predictive Modeling

A Logistic Regression model was developed to predict employee attrition based on the identified factors.

### Model 1: Initial Model (Salary and Department)

*   **Features Used**: `salary`, `Department`
*   **Accuracy**: 55%
*   **Observation**: This initial model provided limited but meaningful predictive signal, suggesting that while salary and department are factors, they alone are not sufficient for highly accurate predictions.

### Model 2: Expanded Feature Set

*   **Features Used**: `satisfaction_level`, `last_evaluation`, `number_project`, `average_monthly_hours`, `time_spend_company`, `Work_accident`, `promotion_last_5years`, `salary`, `Department`
*   **Accuracy**: 67%
*   **Observation**: The inclusion of additional features significantly improved the model's accuracy to 67%. This indicates that a combination of factors, especially including satisfaction and other performance metrics, provides a more comprehensive understanding of attrition.

## Technologies Used

*   **Python**
*   **pandas**: For data manipulation and analysis.
*   **numpy**: For numerical operations.
*   **matplotlib**: For data visualization.
*   **seaborn**: For enhanced data visualizations.
*   **scikit-learn**: For machine learning model development (Logistic Regression) and splitting data.

## How to Run the Analysis

1.  **Clone the Repository**: Download or clone this GitHub repository to your local machine.
2.  **Install Dependencies**: Ensure you have Python installed and install the required libraries using pip:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  **Place Data File**: Make sure the `HR_comma_sep 1.csv` file is in the same directory as your Jupyter notebook/script, or update the file path in the code.
4.  **Execute Notebook**: Open and run the Jupyter notebook (`your_notebook_name.ipynb`) sequentially. The notebook contains all the steps from data loading and cleaning to EDA and model building.

## Future Work

*   **Feature Engineering**: Explore creating new features from existing ones to potentially improve model performance.
*   **Advanced Models**: Experiment with more sophisticated machine learning models (e.g., Random Forest, Gradient Boosting) to achieve higher accuracy.
*   **Hyperparameter Tuning**: Optimize the logistic regression model's hyperparameters.
*   **Addressing Class Imbalance**: Implement techniques like SMOTE or adjust class weights further to improve the model's ability to predict the minority class (employees who leave).
