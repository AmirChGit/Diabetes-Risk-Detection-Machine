# Diabetes Risk Detection Machine Learning Project
![image](https://github.com/user-attachments/assets/2ccf10a4-f30c-4398-b6d9-a909bde9dbd4)

## Introduction
This project introduces a comprehensive approach to utilizing machine learning for identifying individuals at risk of diabetes by analyzing various health indicators. The methodology involves using a dataset that includes key parameters such as BMI, age, smoking status, and physical activity to train a supervised model for predicting diabetes risk. The project also includes the development of an interactive interface for user input and prediction generation.

### Key Aspects of the Project:
1. Utilization of advanced data preprocessing and cleansing methodologies.
2. Conduct of thorough Exploratory Data Analysis (EDA) to uncover relationships within the dataset.
3. Implementation of sophisticated feature selection and engineering techniques.
4. Assessment and comparison of various machine learning models, including Logistic Regression and Random Forest.
5. Integration of an interactive interface for generating predictions based on user input.

### Key Value and Potential Use Cases:
The Diabetes Risk Detection project holds significant value in healthcare analytics, offering use cases such as:
- **Early intervention programs** for high-risk individuals.
- **Personalized healthcare plans** to mitigate diabetes risk factors.
- **Resource allocation optimization** in healthcare systems.
- **Interactive prediction interface** for real-time risk assessment.

---

## Summary of Project Phases and Milestones

### Project Phases:
1. **Data Preprocessing**: Cleaning and optimizing the dataset.
2. **Model Development**: Building and training a supervised model.
3. **Evaluation and Comparison**: Assessing models to determine the best predictor.
4. **Validation and Deployment**: Validating the model and deploying it for real-world use.

### Milestones:
- Completion of data preprocessing and creation of a balanced dataset.
- Development and training of machine learning models.
- Evaluation and selection of the most effective model.
- Validation and deployment in real-world healthcare environments.

---

## Part 1: Data Preprocessing

### Data Preparation and Initial Analysis
This section outlines the steps for cleaning, processing, and exporting datasets.

**Steps:**
1. **Data Cleaning**:
   - Drop missing values.
   - Adjust feature names for readability.
   - Handle specific feature values as follows:
     - **DIABETE4**: Convert to ordinal (0 = no diabetes, 1 = yes diabetes).
     - **_RFHYPE6**: Convert values (1 to 0 for no, 2 to 1 for high blood pressure).
     - **TOLDHI3**: Adjust values and remove invalid entries.
     - **_CHOLCH3**: Modify values for cholesterol checks and remove invalid data.
     - **SMOKE100**: Adjust and clean smoking data.
     - **CVDSTRK3, _MICHD, _TOTINDA, _FRTLT1A**: Similar data cleaning and value adjustments.
2. **Check for Class Imbalance**: Note the distribution of diabetes cases.
3. **Export Cleaned Datasets**: Save datasets as CSV files.

**Binary Dataset Creation:**
- Create a binary dataset for diabetes vs. no diabetes.
- Save both the binary and balanced binary datasets.

---

## Part 2: Machine Learning Models

### Key Components:
1. **Data Preparation and Initial Analysis**
2. **Data Type Optimization and Conversion**
3. **Logistic Regression Model**
4. **Random Forest Model**
5. **Cross-Validation**

### Data Preparation
1. **Feature Removal**: Drop irrelevant features and adjust the "General Health" feature for clarity.
2. **Missing Value Check**: Confirm no missing values.
3. **Data Type Optimization**: Convert numerical values to more efficient data types.

---

### Logistic Regression Model for Diabetes Prediction
1. **Data Scaling**: Use `MinMaxScaler` for scaling features.
2. **Model Training**: Split data into training and test sets, initialize and train the model.
3. **Evaluation**:
   - **Accuracy**: 74.58%
   - **Confusion Matrix**: 
     ```
     [[12556 4657]
      [4101 13143]]
     ```
   - **Classification Report**:
     - Precision: 0.75
     - Recall: 0.73 (False), 0.76 (True)
     - F1-Score: 0.74 (False), 0.75 (True)

4. **Model Export**: Use `joblib` to save and load the trained model.

### Confusion Matrix Visualization
- Generate visualizations to analyze model performance.

---

### Data Exploration
1. **Histograms**: 
   - **Figure 1.a**: General health ratings comparison.
   - **Figure 1.b**: Physical health analysis.
   - **Figure 1.c**: Mental health comparison.
   - **Figure 1.d**: Age distribution analysis.

2. **Scatterplots**:
   - **Figure 2.a**: BMI comparison between diabetics and non-diabetics.
   - **Figure 2.c**: Correlation between physical and mental health.

---

### Random Forest Model for Comparison
1. **Training and Evaluation**: 
   - **Accuracy**: 72.13%
   - **Confusion Matrix**:
     ```
     [[11906 5307]
      [4297 12947]]
     ```
   - **Classification Report**:
     - Precision: 0.73 (False), 0.71 (True)
     - Recall: 0.69 (False), 0.75 (True)
     - F1-Score: 0.71 (False), 0.73 (True)

---

## Cross-Validation of Models
- **KFold Cross-Validation**: Assess model reliability with multiple training/testing cycles.
- Calculate average scores for a robust performance measure.

---

## Patient Outcome Prediction
- **Objective**: Predict diabetes risk using an interactive user interface.
- **Approach**: Users input health indicators, and the system generates predictions to assist in proactive healthcare management.

---

This structured documentation ensures clarity in each project phase, from data preprocessing to model evaluation and prediction.
