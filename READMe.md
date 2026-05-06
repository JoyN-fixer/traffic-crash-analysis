1.  INTRODUCTION

Traffic accidents remain a significant public safety challenge in urban environments, leading to injuries, fatalities, and economic losses. Although large volumes of crash data are collected, it is often difficult for city authorities to extract clear insights about the underlying causes of accidents and the conditions in which they occur.

This project uses integrated crash, vehicle, and people-level data to identify the key factors associated with injury-related crashes.

By applying machine learning techniques, this project aims to:

Predict whether a crash results in injury or no injury
Identify the most influential contributing factors
Translate findings into actionable safety recommendations


2.  BUSINESS UNDERSTANDING

Stakeholder

1. City transportation authority 
2. Road Safety Agencies
3. Urban Planners
4. Emergency Response Teams 

Key Business Questions

This project is designed to answer the following questions:

1. What factors most strongly contribute to injury-related crashes?
2. How do weather, lighting, and road conditions affect crash severity?
3. Do certain vehicle types or manufacturing years correlate with higher crash severity?

3. DATA UNDERSTANDING & PREPARATION

Data Sources:
1. Crashes dataset → accident-level details
2. Vehicles dataset → vehicle-level characteristics
3. People dataset → driver/passenger attributes

Cleaning Steps:
Missing value handling
Standardization of categories
Data type correction
Aggregation to crash-level data

Final dataset includes:
Environmental conditions (weather, lighting, road condition)
Vehicle behavior (maneuver, type, age)
Human factors (age, safety equipment use, sex)
Temporal factors (hour, day, month)

4. MODELLING

i. Target Variable

Binary classification:

0 → No Injury / Drive Away
1 → Injury / Tow Required

ii. Preprocessing Pipeline
Label encoding for categorical variables
SMOTE for class imbalance
Random Forest Classifier for prediction

A Random Forest was chosen because it:

Handles mixed feature types well
Captures nonlinear relationships
Provides feature importance for interpretability

MODEL PERFORMANCE 
Using threshold = 0.52

Performance Summary
Accuracy: ~0.72
Injury Precision: ~0.49
Injury Recall: ~0.49
F1-score (Injury): ~0.49

INSIGHTS

1. Majority of crashes do NOT result in injury
2. Injury crashes are less predictable and influenced by complex factors not fully captured in the dataset.
3. Traffic congestion and human behavior patterns strongly influence crash likelihood.
4. Model performance is constrained by limited behavioral and real-time traffic data.

RECOMMENDATIONS
1. Using advanced models 
2. Incorporate real time traffic data
3. Increased patrol during peak hours