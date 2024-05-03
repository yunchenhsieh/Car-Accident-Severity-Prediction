# Car Accident Severity Prediction 

# Project Description:
We intend to build a ML pipeline in Apache Spark to predict car severity based on weather condition and traffic information, enabling stakeholders to take proactive measures for road safety.

# Data (2023 March):
The dataset is composed of 500K instances, each comprising car severity alongside real-time weather conditions and traffic information

# Data Engineering:
1. Drop null value
2. Filter out outliers (apply Interquartile Range (IQR))
3. Replace zero values with their second minimal counterparts (zero values likely represent data errors)
4. Simplify severity levels by categorizing 0 and 1 as 0, and 3 and 4 as 1,
5. Oversample the data: Make data balanced

# ML pipeline:
- StringIndexer: convert categorical string columns into numerical indices.  
- One Hot Encoder: convert categorical variables into a binary vector representation  
- Normalizer: Z-score normalization  
- Vector Assembler:  aggregate multiple columns into a single feature vector  
- Model:  
i. Logistc Regression(AUC: 0.69)  
ii. Random Forest(AUC: 0.73)  
iii. SVM Model(AUC: 0.69)  
