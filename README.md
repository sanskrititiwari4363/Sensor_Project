Sensor Anomaly Detection using Machine Learning
Project Overview

This project focuses on detecting anomalies in an energy manufacturing plant using Machine Learning techniques. The dataset contains sensor readings collected at different time intervals. The goal is to predict whether a machine condition is normal or anomalous based on sensor values.

This project includes:

Data preprocessing
Feature engineering
Exploratory Data Analysis (EDA)
Multiple Machine Learning models
Model evaluation using F1-score
Final prediction generation
Problem Statement

Energy manufacturing plants use sensors to continuously monitor machine conditions. Abnormal sensor behavior may indicate machine faults or failures.

The objective of this project is to build a Machine Learning model that can accurately classify:

0 → Normal Condition
1 → Anomaly Detected

using sensor readings from:

X1
X2
X3
X4
X5
Dataset Information

Dataset Files:

train.parquet
test.parquet
sample_submission.parquet

Columns:

Column	Description
Date	Timestamp of sensor reading
X1	Sensor 1 reading
X2	Sensor 2 reading
X3	Sensor 3 reading
X4	Sensor 4 reading
X5	Sensor 5 reading
target	0 = Normal, 1 = Anomaly
Technologies Used
Python
Jupyter Notebook
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
XGBoost
LightGBM
CatBoost
Project Workflow
1. Data Loading
Loaded .parquet files using Pandas
2. Data Preprocessing
Converted Date column into datetime format
Handled missing values
Removed unnecessary columns
Standardized numerical features
3. Feature Engineering

Created additional features such as:

Year
Month
Day
Hour
Day of Week
Sensor Mean
Sensor Standard Deviation
Sensor Energy
Sensor Range
Interaction Features
Ratio Features
4. Exploratory Data Analysis

Performed:

Target distribution analysis
Correlation heatmap
Feature importance visualization
5. Machine Learning Models Used
Logistic Regression
Support Vector Machine (SVM)
Decision Tree
Random Forest
LightGBM
CatBoost
6. Model Evaluation

Models were evaluated using:

Accuracy
Precision
Recall
F1-Score
Classification Report
Best Model

CatBoost Classifier was selected as the final model based on overall performance and anomaly detection capability.

Feature Engineering Highlights

Additional engineered features:

sensor_mean
sensor_std
sensor_min
sensor_max
sensor_energy
sensor_range
X1_X2
X3_X4
X5_div_X1

These features helped improve model learning and anomaly detection performance.

Output

Final predictions were saved in:

submission.parquet
How to Run the Project
Install Required Libraries
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm catboost pyarrow
Run Jupyter Notebook
jupyter notebook
Open the Notebook

Run all cells sequentially.

Project Structure
Sensor_Project/
│
├── train.parquet
├── test.parquet
├── sample_submission.parquet
├── submission.parquet
├── Sensor_Anomaly_Detection.ipynb
├── README.md
Future Improvements
Hyperparameter tuning
Cross-validation
Time-series based anomaly detection
Deep Learning approaches
Advanced ensemble methods
Learning Outcomes

Through this project, I learned:

Data preprocessing techniques
Feature engineering
Model training and evaluation
Handling imbalanced datasets
Anomaly detection using ML
Working with parquet files
Building end-to-end ML workflows
Conclusion

This project demonstrates how Machine Learning can be applied to detect anomalies in industrial sensor data. By combining preprocessing, feature engineering, and multiple ML models, the system can effectively identify abnormal machine behavior and support predictive maintenance applications.

Author

Sanskriti Tiwari
