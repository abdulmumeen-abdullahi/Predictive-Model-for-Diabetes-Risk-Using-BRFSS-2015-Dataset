# Predictive Modeling for Diabetes Risk Assessment

An interactive web application powered by an XGBoost model to predict diabetes risk based on health indicators from the BRFSS 2015 dataset.

<img width="1366" height="768" alt="400217756-1e5d3461-aa43-4fdb-8b9a-75686554b554" src="https://github.com/user-attachments/assets/d840a2cf-b198-4201-b378-0ef4c855352f" />

## 📖 Project Overview

> Diabetes is a widespread chronic disease affecting millions of Americans annually, imposing a significant financial burden on the economy. It impairs the body's ability to regulate blood glucose levels, leading to severe health complications such as heart disease, vision loss, limb amputation, and kidney disease. Diabetes occurs when the body either fails to produce sufficient insulin or cannot use insulin effectively.

While there is no cure for diabetes, early detection and lifestyle changes can help manage the disease effectively. This project aims to develop a predictive model to detect the likelihood of diabetes based on key health indicators. By leveraging this model, individuals, healthcare providers, and policymakers can better manage health outcomes, allocate resources more effectively, and implement timely interventions.


## 📊 Dataset Overview

The dataset used in this project originates from the Behavioral Risk Factor Surveillance System (BRFSS), an annual telephone survey conducted by the CDC. The 2015 BRFSS dataset, sourced from [Kaggle](https://www.kaggle.com/datasets/abdelazizsami/cdc-diabetes-health-indicators), contains responses from **70,692 individuals** across **22 features** related to health, lifestyle, and socioeconomic factors.


## ✨ Features Used

After correlation analysis, the following 11 features were selected due to their strong correlation with the target variable (**Diabetes_binary**):

* **HighBP**: Indicates if an individual has been diagnosed with high blood pressure (1) or not (0).
* **HighChol**: Indicates if an individual has been diagnosed with high cholesterol levels (1) or not (0).
* **BMI**: A numerical value representing the individual's body mass index.
* **HeartDiseaseorAttack**: Indicates if an individual has ever had heart disease or a heart attack (1) or not (0).
* **PhysActivity**: Indicates if an individual engages in regular physical activity (1) or not (0).
* **GenHlth**: Self-reported general health status, ranging from 1 (Excellent) to 5 (Poor).
* **PhysHlth**: Number of days in the past month when physical health was reported as "not good."
* **DiffWalk**: Indicates if an individual has difficulty walking or climbing stairs (1) or not (0).
* **Age**: Represents the age of the individual.
* **Education**: Represents the individual's highest level of education.
* **Income**: Represents the individual's income level.

## 🛠️ Methodology

1.  **Data Preprocessing**: The dataset was loaded into a Pandas DataFrame. The `Age` column was adjusted for better realism, and all feature data types were converted to `int` for streamlined processing.
2.  **Exploratory Data Analysis (EDA)**: A correlation matrix and heatmap were generated to identify relationships between features and the target variable. `GenHlth` (Correlation: 0.41) and `HighBP` (Correlation: 0.38) showed the strongest correlations.
3.  **Model Training and Selection**: The dataset was split into training (80%) and testing (20%) sets. Multiple models were evaluated, with the **XGBoost Classifier** demonstrating the highest accuracy. The model was optimized using hyperparameter tuning.

## 📈 Model Performance

The final XGBoost Classifier achieved a **75% accuracy** on the test set.

* **Precision**: 0.78 (Class 0), 0.73 (Class 1)
* **Recall**: 0.70 (Class 0), 0.80 (Class 1)
* **F1-Score**: 0.74 (Class 0), 0.76 (Class 1)

The confusion matrix below visualizes the model's performance:

<img width="516" height="432" alt="400416926-ff6eaf68-df60-40f3-87aa-14b555a95aa8" src="https://github.com/user-attachments/assets/62abdbc4-230e-4052-beb9-e1a6c7144341" />

## 💡 How the Model Benefits Stakeholders

This predictive tool offers significant benefits:

* **Early Detection**: Identifies at-risk individuals, enabling timely interventions.
* **Personalized Health Insights**: Provides tailored recommendations for healthier lifestyles.
* **Cost Reduction**: Reduces healthcare costs by focusing on early management and preventing complications.
* **Efficient Resource Allocation**: Helps healthcare providers prioritize high-risk patients.
* **Supporting SDGs**: Contributes to **Sustainable Development Goal (SDG) 3: Good Health and Well-being**.


## ⚠️ Limitations and Ethical Considerations

* **Data Authenticity**: The dataset's reliability cannot be fully guaranteed, making the model unsuitable for real-world deployment without further validation.
* **Ethical Use**: Predictions should supplement, not replace, professional medical advice.

## ✅ Conclusion

This project highlights the potential of machine learning in healthcare to address pressing issues like diabetes management. By integrating this predictive model into healthcare systems, we can reduce costs, improve health outcomes, and contribute to equitable healthcare practices.
