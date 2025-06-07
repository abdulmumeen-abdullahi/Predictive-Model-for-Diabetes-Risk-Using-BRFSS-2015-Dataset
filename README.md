# Predictive Modeling for Diabetes Risk Assessment Using Health Indicators and Behavioral Risk Factors for Early Intervention
## Project Overview
Diabetes is a widespread chronic disease affecting millions of Americans annually, imposing a significant financial burden on the economy. It impairs the body's ability to regulate blood glucose levels, leading to severe health complications such as heart disease, vision loss, limb amputation, and kidney disease. Diabetes occurs when the body either fails to produce sufficient insulin or cannot use insulin effectively—an essential hormone that enables cells to use sugar from the bloodstream for energy.

While there is no cure for diabetes, early detection, lifestyle changes, and medical treatments can help manage the disease effectively. This project aims to develop a predictive model to detect the likelihood of diabetes based on health indicators. By leveraging this model, individuals, healthcare providers, and policymakers can manage health outcomes better, allocate resources more effectively, and implement timely interventions.

## Dataset Overview
The dataset used in this project originates from the Behavioral Risk Factor Surveillance System (BRFSS), an annual telephone survey conducted by the CDC. The 2015 BRFSS dataset, sourced from [Kaggle](https://www.kaggle.com/datasets/abdelazizsami/cdc-diabetes-health-indicators), contains responses from 70,692 individuals across 22 features related to health, lifestyle, and socioeconomic factors.

## Features Used
After correlation analysis, the following 11 features were selected due to their strong correlation with the target variable (Diabetes_binary):

1. Diabetes_binary (Target Variable): Indicates whether an individual has been diagnosed with diabetes (1) or not (0).
2. HighBP (High Blood Pressure): Indicates if an individual has been diagnosed with high blood pressure (1) or not (0).
3. HighChol (High Cholesterol): Indicates if an individual has been diagnosed with high cholesterol levels (1) or not (0).
4. BMI (Body Mass Index): A numerical value representing the individual's body mass index, calculated from height and weight, used as an indicator of body fatness.
5. HeartDiseaseorAttack: Indicates if an individual has ever had a heart disease or heart attack (1) or not (0).
6. PhysActivity (Physical Activity): Indicates if an individual engages in regular physical activity (1) or not (0).
7. GenHlth (General Health): Self-reported general health status, ranging from 1 (Excellent) to 5 (Poor).
8. PhysHlth (Physical Health): Number of days in the past month when physical health was reported as "not good."
9. DiffWalk (Difficulty Walking): Indicates if an individual has difficulty walking or climbing stairs (1) or not (0).
10. Age: Represents the age of the individual ranging from 1 to 13.
11. Education: Represents the individual's highest level of education, encoded as a categorical variable ranging from 1 (Less than High School) to 6 (Doctorate Degree).
12. Income: Represents the individual's income level, encoded as a categorical variable ranging from 1 (Very Low Income) to 8 (Top Income).

## Methodology
### 1. Data Preprocessing
- Loaded the dataset into a Pandas DataFrame.
- Modified the Age column by adding 48 to each value for better realism, as the original values ranged from 1 to 13, which were not intuitive.
- Converted all feature values from float to int to streamline data processing.
### 2. Exploratory Data Analysis (EDA)
Generated a correlation matrix and a heatmap to identify relationships between features and the target variable.
Notable correlations:
- GenHlth (Correlation: 0.41)
- HighBP (Correlation: 0.38)

![download](https://github.com/user-attachments/assets/78bdc979-ca13-4997-a327-36292f7805ef)

### 3. Model Training
- Split the dataset into training (80%) and testing (20%) sets.
- Established a baseline model using the normalized value count of the target variable, yielding a benchmark accuracy of 50.04%.
### 4. Model Selection and Evaluation
Trained and evaluated multiple machine learning models, including:
- XGBoost Classifier (Highest Accuracy: 75%)
- Logistic Regression
- Random Forest Classifier
- Decision Tree Classifier
Applied hyperparameter tuning to optimize model performance, calculating MAE for each model.
### 5. Classification Report and Confusion Matrix
The XGBoost Classifier achieved:

- Precision = 0.78 for 0 class and 0.73 for 1 class </br>
- Recall = 0.70 for 0 class and 0.80 for 1 class </br>
- F1-Score = 0.74 for 0 class and 0.76 for 1 class </br>
- True Negatives = 4994, True Positives = 5610, False Negatives = 2096, False Positives = 1439.

![download](https://github.com/user-attachments/assets/ff6eaf68-df60-40f3-87aa-14b555a95aa8)

## Interactive Dash Application
A user-friendly interactive web application was developed using Dash, featuring:
- Inputs: HighBP, HighChol, BMI, HeartDiseaseorAttack, PhysActivity, GenHlth, PhysHlth, DiffWalk, Age, Education, Income, and Sex.
- Output: Real-time diabetes risk prediction based on user-provided inputs.

![BRFSS2015 Diabetes Prediction Dashboard](https://github.com/user-attachments/assets/1e5d3461-aa43-4fdb-8b9a-75686554b554)

### Features of the Application:
- Intuitive input fields for data entry, including dropdowns and number boxes.
- Real-time prediction displayed upon clicking "Predict."

## How the Model Benefits Stakeholders
This predictive diabetes model is a valuable tool for individuals, healthcare providers, and policymakers, offering the following benefits:
### 1. Early Detection
Identifies individuals at risk, enabling timely interventions to prevent or manage diabetes effectively.
### 2. Personalized Health Insights
Provides tailored recommendations for individuals to adopt healthier lifestyles.
### 3. Cost Reduction
Reduces healthcare costs by preventing complications and focusing on early management.
### 4. Efficient Resource Allocation
Helps healthcare providers prioritize high-risk patients, optimizing the allocation of resources.
### 5. Data-Driven Decisions
Equips medical practitioners with actionable insights to enhance diagnosis and treatment strategies.
### 6. Supporting SDGs
Contributes to Sustainable Development Goal (SDG) 3: Good Health and Well-being by improving early detection, reducing diabetes-related complications, and addressing healthcare disparities.

## Limitations and Ethical Considerations
While this model demonstrates robust predictive capabilities, it is important to note:

- Data Authenticity: The dataset's reliability cannot be fully guaranteed, making the model unsuitable for real-world deployment without further validation.
- Ethical Use: Predictions should supplement, not replace, professional medical advice.

## Conclusion
This project highlights the potential of machine learning in healthcare to address pressing issues like diabetes management. By incorporating this predictive model into healthcare systems, we can reduce costs, improve health outcomes, and contribute to equitable healthcare practices.

Abdullahi Olalekan Abdulmumeen </br>
Applied Data Scientist </br>
📧 olalekanabdulmumeen3@gmail.com </br>

#### Note:
This model is a proof of concept and not intended for real-world deployment. For a custom, robust predictive model tailored to your specific needs, feel free to reach out.
