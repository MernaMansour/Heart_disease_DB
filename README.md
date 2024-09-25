# Heart Disease Prediction using Semi-Supervised Learning
## Project Overview
This project leverages semi-supervised learning techniques to predict heart disease from clinical data. In real-world scenarios, obtaining labeled data can be costly and time-consuming. To address this challenge, the project uses both labeled and unlabeled data to improve the predictive accuracy of the model. The semi-supervised learning methods employed include Label Propagation, Label Spreading, and Self-Training with SVM.
## Objective
The objective of this project is to build an advanced machine learning model to predict heart disease by utilizing semi-supervised learning techniques. By using both labeled and unlabeled data, the goal is to increase the model’s generalization capability when labeled data is limited.
## Data Description
The dataset contains various clinical features used for predicting heart disease. The key features in the dataset include:
##### 1. Age
##### 2. Sex:
* Values:  
1: Male  
0: Female
##### 3. Chest Pain Type:
* Description: 
Type of chest pain experienced by the patient.    
* Values:  
1: Typical angina
2: Atypical angina
3: Non-anginal pain
4: Asymptomatic
##### 4. Resting Blood Pressure:
* Description: Resting blood pressure in mm Hg.  
* Values: Continuous numerical values (e.g., 120.0, 160.0).  
##### 5. Cholesterol:
* Description: Serum cholesterol in mg/dl.  
* Values: Continuous numerical values (e.g., 204.0, 300.0).
##### 6. Fasting Blood Sugar:
* Description: Fasting blood sugar > 120 mg/dl.  
* Values:  
1: True  
0: False  
##### 7. Resting ECG Results:
* Description: Results of the resting electrocardiogram.  
* Values:  
0: Normal  
1: Having ST-T wave abnormality  
2: Showing probable or definite left ventricular hypertrophy
##### 8. Maximum HR Achieved:
* Description: Maximum heart rate achieved by the patient.  
* Values: Continuous numerical values (e.g., 150.0, 180.0).
##### 9. Angina:
* Description: Exercise induced angina.  
* Values:  
1: Yes  
0: No
##### 10. ST Depression:
* Description: ST depression induced by exercise relative to rest.  
* Values: Continuous numerical values (e.g., 2.3, 3.0).  
##### 11. Slope of Peak Exercise ST Segment:
* Description: Slope of the peak exercise ST segment.  
* Values:  
1: Upsloping    
2: Flat   
3: Downsloping  
##### 12. Number of Major Vessels:
* Description: Number of major vessels colored by fluoroscopy.  
* Values: Integer values from 0 to 3.  
##### 13. Thalassemia:
* Description: Thalassemia status.  
* Values:  
1: Normal (no thalassemia)   
2: Minor thalassemia  
3: Moderate thalassemia  
4: Severe thalassemia  
5: Thalassemia major  
6: Another specific type of thalassemia (like hemoglobin E or similar)  
7: Unknown or other  
##### 14. Heart Disease:
* Description: Diagnosis of heart disease.
* Values:
1: No heart disease  
2: Heart disease present (mild)  
3: Heart disease present (moderate)  
4: Heart disease present (severe)
## Project Workflow
### 1. Data Preprocessing
* Missing values are handled for both numerical and categorical features.
* Numerical features are standardized using StandardScaler.
* Categorical features are converted into appropriate formats.
* 30% of the labels in the target (Heart Disease) are masked as unlabeled to simulate real-world scenarios.
### 2. Visualization and Analysis
Various visualizations (scatter plots, boxplots, countplots, etc.) are generated to analyze the relationships between features such as Sex and Heart Disease, Resting Blood Pressure and Cholesterol, etc.
A correlation matrix is created to assess the relationships between numerical features and their correlation with the target variable.
### 3. Modeling
* Label Propagation: This method is used to propagate labels through the graph structure of the data.
* Label Spreading: Similar to Label Propagation but with a regularization term to improve label diffusion.
* Self-Training with SVM: A semi-supervised approach where an SVM model is trained on labeled data, and then iteratively adds predictions on unlabeled data to the training set.
### 4. Evaluation
The performance of each model is evaluated using metrics such as accuracy, confusion matrix, and classification report.
Visualizations such as confusion matrices and pair plots are used to interpret the results.
