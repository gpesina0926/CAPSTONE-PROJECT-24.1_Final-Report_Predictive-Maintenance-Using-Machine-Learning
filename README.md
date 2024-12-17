Predictive Maintenance Using Machine Learning
1. Define the Problem Statement
In manufacturing, unexpected equipment failures result in significant downtime, increased costs, and production inefficiencies. The goal of this project was to develop a predictive maintenance solution that leverages machine learning to detect failures before they occur. By analyzing historical and real-time sensor data, the solution aims to optimize maintenance schedules, reduce operational disruptions, and improve resource efficiency.

3. Model Outcomes or Predictions
This project focused on a classification problem using supervised machine learning algorithms to predict equipment failures. The models output whether a machine will fail (failure = 1) or not fail (non-failure = 0).

Key Models Used:
- Logistic Regression
- Random Forest
- Gradient Boosting
- LightGBM

Outcome: The LightGBM model achieved the best performance with an F1 Score of 0.69 and a recall of 85%, ensuring that most failures were successfully detected.

3. Data Acquisition
The project used the AI4I 2020 Predictive Maintenance Dataset from the UC Irvine Machine Learning Repository. This dataset includes:
- Machine sensor readings (e.g., torque, rotational speed, temperature)
- Operational metrics
- Failure types (e.g., tool wear, heat dissipation, power failures)

Data Visualization:
- Correlation Matrix: Showed strong relationships between process temperature and air temperature.
- Bivariate Analysis: Highlighted key patterns, such as the impact of Tool Wear and Torque on machine failures.
- Chi-Square Tests: Confirmed significant associations between specific failure types (tool wear, power issues) and machine breakdowns.
- 
4. Data Preprocessing/Preparation
The following steps were taken to clean and prepare the data:

a. Handling Missing Values and Outliers:
- Data was clean with no missing values.
- Outliers in key features like Torque and Rotational Speed were capped at the 99th percentile to reduce noise.

b. Data Splitting:
- The data was split into training (80%) and test sets (20%) to evaluate model performance.

c. Feature Engineering:
- Temperature Delta: Difference between process and air temperature to identify overheating risks.
- Vibration Indicator: Combined rotational speed and torque to measure machine stress.
- Tool Wear Categorization: Simplified tool wear levels into Low, Medium, and High Wear for better interpretability.
- 
5. Modeling
The following supervised learning models were tested to predict failures:
1. Logistic Regression: Simple but struggled with imbalanced data (F1 Score = 0.21).
2. Random Forest: Reliable, handled complex data well (F1 Score = 0.73).
3. Gradient Boosting: Accurate but slower to build (F1 Score = 0.73).
4. LightGBM: Best performer, balancing speed and accuracy (F1 Score = 0.69, Recall = 85%).

Why LightGBM?
LightGBM’s efficiency and ability to handle uneven data made it ideal for predicting rare failure events.

6. Model Evaluation
The models were evaluated using:
- F1 Score: Balances precision and recall to provide a single measure of accuracy.
- Recall: Prioritized to minimize missed failures (false negatives), as failing to detect an issue could lead to costly downtimes.

Key Results:
- LightGBM achieved the best recall (85%), successfully identifying most failures while maintaining a balanced F1 score.
- Precision was 47%, indicating some false alerts, which are acceptable in preventive maintenance scenarios.
- 
Suggestions for Next Steps
1. Enhance Data Collection: Incorporate additional sensor readings, maintenance logs, and environmental factors to improve model accuracy.
2. Monitor Model Performance: Continuously evaluate the model with real-time data to ensure reliability and accuracy.
3. Refine Alert Systems: Address false positives by improving precision through further model tuning.
4. Scale Deployment: Deploy the model across all critical equipment to maximize operational efficiency and reduce unexpected down
