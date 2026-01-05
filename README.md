MACHINE LEARNING APPLICATION IN EARLY WARNING HEART DISEASE DETECTION

Heart Failure Mortality Prediction Using Explainable Machine Learning
Problem Statement
Early identification of high-risk heart failure patients is critical for timely clinical intervention. This project aimed to develop an interpretable machine learning model capable of risk stratification and mortality prediction, with an emphasis on sensitivity to avoid missing high-risk patients.

Clinical and demographic variables included:

Age, sex, Ejection fraction, Serum creatinine, serum sodium, Platelets, Creatinine phosphokinase, Comorbidities (diabetes, anaemia, hypertension, smoking), Follow-up time

Exploratory Data Analysis

EDA revealed clinically consistent patterns:
Mortality clustered in older patients (60–75), Lower ejection fraction, elevated creatinine, and hyponatremia were associated with death, Shorter follow-up time strongly correlated with mortality, These patterns informed model expectations and validation.

Correlation Analysis

A correlation heatmap showed low multicollinearity among predictors, with the strongest associations to mortality observed for:
Time (r ≈ −0.53)
Serum creatinine (r ≈ +0.29)
Ejection fraction (r ≈ −0.27)
Age (r ≈ +0.25)
This supported the use of nonlinear tree-based models.

Modeling Approach

A Random Forest classifier was trained using:
Increased tree depth
Class weighting to penalize false negatives
Feature subsampling to improve minority-class learning

Threshold Optimization

Rather than relying on the default 0.5 cutoff, the decision threshold was optimized using the Precision–Recall curve to prioritize recall.
This allowed the model to better capture high-risk patients while maintaining acceptable precision.
Feature importance analysis showed the strongest predictors were:

Follow-up time
Serum creatinine
Ejection fraction
Platelets
Age
Serum sodium
These aligned with EDA and known clinical risk factors, reinforcing model interpretability.

Conclusion

This project demonstrates an end-to-end, explainable ML pipeline where:
EDA, correlation analysis, and feature importance align
Model behavior is transparent and clinically plausible
Threshold tuning enables risk-sensitive decision-making
The final model is best suited for clinical risk stratification and early warning, rather than binary diagnosis.
