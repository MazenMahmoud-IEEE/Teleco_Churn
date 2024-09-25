1. **Project Title**
2. **Project Description**
3. **Dataset Information**
4. **Project Objectives**
5. **Project Workflow**
6. **Modeling Process**
7. **Evaluation Metrics**
8. **How to Use the Code**
9. **Installation Instructions**
10. **Contributing**
11. **License**

### 1. Project Title

**Telecom Customer Churn Prediction**

### 2. Project Description

This project aims to predict customer churn in a telecom company using various machine learning algorithms. Customer churn refers to the process of customers discontinuing their services with the company. The project leverages features such as customer demographics, account details, and service usage to identify patterns leading to churn.

### 3. Dataset Information

The dataset used for this project is from Kaggle's Telecom Churn dataset. It contains customer-level information, including:

- **Demographics:** Senior citizen status, presence of partners and dependents.
- **Services used:** Type of internet service, whether online security, tech support, and other additional services were subscribed.
- **Account details:** Contract type, payment method, and total charges.

Key features used for prediction include:

- `InternetService_Fiber optic`
- `PaymentMethod_Electronic check`
- `MonthlyCharges`
- `SeniorCitizen`
- `TechSupport_Yes`
- `Contract_One year`
- `TotalCharges`
- `tenure`

### 4. Project Objectives

The primary objective is to create a machine learning model that accurately predicts whether a customer will churn, enabling the company to take preemptive action.

### 5. Project Workflow

The workflow follows a standard data science pipeline:

1. **Data Collection & Exploration:** 
   - The data is first loaded and inspected for missing values and anomalies.
   - Exploratory Data Analysis (EDA) is performed to understand feature distributions and relationships with churn.
   
2. **Data Preprocessing:**
   - Handling missing values.
   - Converting categorical variables into numerical formats (One-Hot Encoding).
   - Exploratory Data Analysis (EDA) is performed to understand feature distributions and relationships with churn.


3. **Model Selection:**
   - Multiple models were tested, including Decision Trees, Random Forest, SVM, LightGBM, and XGBoost.
   - The Random Forest classifier was found to perform the best.

4. **Model Tuning:**
   - Hyperparameter tuning was performed using GridSearchCV to find the optimal model parameters.
   - The model was evaluated based on accuracy, precision, recall, and F1-score, focusing on maximizing the F1-score due to the imbalanced nature of the dataset.

### 5. Modeling Process

#### Algorithms Tried:

- **Decision Tree:** Simple baseline model.
- **Random Forest:** Chosen for its high accuracy (77%) and strong F1-score (62%) after tuning.
- **XGBoost & LightGBM:** Gradient boosting models with reasonable performance but not superior to Random Forest.

#### Best Model:

The **Random Forest Classifier** was selected as the final model, with an F1-score of 62% and maximum accuracy of 77%.

#### Hyperparameters Tuned:

- Number of trees in the forest (`n_estimators`).
- Maximum depth of trees (`max_depth`).
- Minimum samples required to split a node (`min_samples_split`).

### 6. Evaluation Metrics

The model performance was evaluated using:

- **Accuracy:** The overall correctness of the model’s predictions.
- **F1-score:** Focused on precision and recall for imbalanced classes.


### 7. How to Use the Code

#### Running the Code:

To run this project on your local machine:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/telecom-churn-prediction.git
   cd telecom-churn-prediction
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook to execute the code:
   ```bash
   jupyter notebook Tele_Churn_Script.ipynb
   ```

4. Use the pre-trained model or retrain it with:
   ```bash
   python churn_model.py
   ```

### 8. Installation Instructions

The project requires Python 3.x and the following Python libraries:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

You can install all dependencies using:
```bash
pip install -r requirements.txt
```

### 9. Contributing

Contributions are welcome! If you would like to contribute, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

### 10. License

This project is licensed under the MIT License. See the LICENSE file for details.
