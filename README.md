# ship-engine-anomaly-detection
Anomaly detection in ship engine sensor data using IQR, One-Class SVM, and Isolation Forest
Ship Engine Anomaly Detection Using Statistical and Machine Learning Methods
Project Overview

This project investigates anomalous activity in ship engine sensor data using both statistical and machine learning approaches.

The objective was to identify abnormal operating conditions that could indicate engine faults, maintenance requirements, safety risks, or reduced operational efficiency.

Business Context

Ship engine failures can result in:

Increased fuel consumption
Higher maintenance costs
Safety risks
Delayed deliveries
Reduced customer satisfaction

An effective anomaly detection system can support predictive maintenance and improve fleet reliability.

Dataset

The dataset contained 19,535 observations and six continuously monitored engine parameters:

Engine RPM
Lubrication Oil Pressure
Fuel Pressure
Coolant Pressure
Lubrication Oil Temperature
Coolant Temperature
Exploratory Data Analysis

The following steps were performed:

Missing value assessment
Duplicate record assessment
Descriptive statistics
Mean and median analysis
Distribution visualisation
Percentile analysis
Outlier exploration

No missing values or duplicate records were identified.

Statistical Anomaly Detection
Interquartile Range (IQR)

The IQR method was used to identify outliers for each sensor feature.

Binary anomaly indicators were created for every feature.

Different anomaly thresholds were evaluated based on the number of features simultaneously exhibiting outlier behaviour.

Key Findings
Samples with anomalies in two or more features represented approximately 2.16% of observations.
Samples with anomalies in three or more features represented approximately 0.05% of observations.

This aligns with the expected anomaly range of 1–5%.

Machine Learning Approaches
One-Class SVM

Features were scaled using Min-Max Scaling before modelling.

Model hyperparameters including gamma and nu were adjusted to obtain anomaly rates within the expected range.

Isolation Forest

Isolation Forest was applied as an alternative unsupervised anomaly detection method.

The contamination parameter was tuned to achieve anomaly rates between 3% and 5%.

Dimensionality Reduction and Visualisation

Principal Component Analysis (PCA) was used to reduce six-dimensional sensor data into two dimensions for visualisation.

Scatter plots were used to visualise anomalous observations identified by:

One-Class SVM
Isolation Forest
Results
IQR Method
Effective for identifying univariate outliers
Simple and interpretable
Limited in capturing complex relationships between features
One-Class SVM
Detected approximately 3–5% anomalous observations
Captured non-linear relationships
Sensitive to hyperparameter selection
Isolation Forest
Produced stable anomaly detection performance
Efficient on larger datasets
Successfully identified observations with unusual combinations of sensor readings
Key Skills Demonstrated
Python
Exploratory Data Analysis
Feature Engineering
Anomaly Detection
One-Class SVM
Isolation Forest
PCA
Data Visualisation
Predictive Maintenance Analytics
Potential Healthcare Applications

The same anomaly detection techniques can be applied to:

Patient monitoring systems
Early disease detection
Medical device monitoring
Healthcare operational analytics
Clinical risk identification
Molecules with unusual properties
Novel compounds outside the normal chemical space
