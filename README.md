
# 🚗 Ford Car Price Prediction using Machine Learning

## 📌 Project Overview

This project focuses on analyzing Ford car data and predicting car prices using Machine Learning techniques.

The project includes **Exploratory Data Analysis (EDA)**, data preprocessing, one-hot encoding, feature scaling, and Linear Regression to understand the factors affecting car prices.

The main objective is to build a regression model that predicts the price of a Ford car based on its features.

---

## 🎯 Objectives

- Analyze the Ford car dataset.
- Perform Exploratory Data Analysis (EDA).
- Identify relationships between car features and price.
- Handle categorical variables using One-Hot Encoding.
- Scale numerical features using StandardScaler.
- Train a Linear Regression model.
- Evaluate model performance using the R² score and Adjusted R² score.

---

## 📂 Dataset

The dataset contains information about Ford cars and their features.

### Features Used

| Feature | Description |
|---|---|
| `model` | Model of the car |
| `year` | Manufacturing year |
| `price` | Price of the car (Target Variable) |
| `transmission` | Type of transmission |
| `mileage` | Distance travelled by the car |
| `fuelType` | Type of fuel used |
| `tax` | Vehicle tax |
| `mpg` | Miles per gallon |
| `engineSize` | Engine size |

**Target Variable:** `price`

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 🔍 Project Workflow

### 1. Data Loading

The Ford car dataset is loaded using Pandas.

```python
import pandas as pd

df = pd.read_csv("ford.csv")
```

### 2. Exploratory Data Analysis (EDA)

The dataset is analyzed using:

- Dataset shape and information
- Descriptive statistics
- Missing value checking
- Histograms
- Correlation matrix
- Heatmaps
- Boxplots
- Scatter plots

These techniques help explore the distribution of car prices and relationships between different features.

### 3. Data Preprocessing

The following preprocessing techniques are applied:

- Separating input features (X) and target variable (y).
- One-Hot Encoding for categorical columns.
- Converting encoded values into integer format.
- Standardizing numerical features using `StandardScaler`.

### 4. Train-Test Split

The dataset is divided into training and testing sets.

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X_one_encode,
    y,
    test_size=0.2,
    random_state=42
)
```

- Training data: 80%
- Testing data: 20%
- Random state: 42

### 5. Model Training

Linear Regression is used to predict car prices.

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(X_train, y_train)
```

### 6. Prediction

The trained model is used to predict prices for the test dataset.

```python
y_pred = model.predict(X_test)
```

### 7. Model Evaluation

The model is evaluated using:

- R² Score
- Adjusted R² Score

```python
from sklearn.metrics import r2_score

r2 = r2_score(y_test, y_pred)

n = X_test.shape[0]
p = X_test.shape[1]

adjusted_r2 = 1 - (
    ((1 - r2) * (n - 1)) / (n - p - 1)
)

print("R² Score:", r2)
print("Adjusted R² Score:", adjusted_r2)
```

---

## 📊 Exploratory Data Analysis

The following visualizations are included in the project:

- Price distribution histogram
- Correlation matrix
- Correlation heatmap
- Price vs. year boxplot
- Mileage vs. price scatter plot
- Engine size vs. price boxplot
- Transmission vs. price boxplot
- Fuel type vs. price boxplot
- Model vs. price boxplot

These visualizations help investigate patterns and relationships within the dataset.

---

## 📈 Model Performance

The model performance is evaluated using the R² Score and Adjusted R² Score.

| Evaluation Metric | Result |
|---|---|
| R² Score | Run notebook to calculate |
| Adjusted R² Score | Run notebook to calculate |

> Note: The evaluation scores should be updated with the actual values obtained from running the notebook.

---

## 📁 Project Structure

```text
Ford-Car-Price-Prediction/
│
├── ford_car_price_prediction.ipynb
├── ford.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository.git
```

### 2. Navigate to the Project Folder

```bash
cd Ford-Car-Price-Prediction
```

### 3. Install Required Libraries

```bash
pip install pandas numpy seaborn matplotlib scikit-learn jupyter
```

### 4. Open Jupyter Notebook

```bash
jupyter notebook
```

### 5. Run the Notebook

Open the notebook and execute the cells to perform data analysis, train the model, and evaluate its performance.

---

## 💡 Key Learnings

Through this project, I learned:

- Fundamentals of Exploratory Data Analysis.
- Data preprocessing and feature engineering.
- One-Hot Encoding for categorical data.
- Feature scaling using StandardScaler.
- Splitting data into training and testing sets.
- Building a Linear Regression model.
- Evaluating regression models using R² and Adjusted R².

---

## 🔮 Future Improvements

- Compare Linear Regression with Random Forest Regression.
- Apply additional regression algorithms.
- Use Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
- Perform hyperparameter tuning for suitable models.
- Improve feature selection.
- Deploy the model using Streamlit.

---

