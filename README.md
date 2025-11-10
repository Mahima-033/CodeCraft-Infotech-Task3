# CodeCraft-Infotech-Task3
A Decision Tree classifier was developed to predict customer subscription to term deposits ("yes" or "no") for a bank's marketing campaign. The model achieved 88.48% overall accuracy using entropy as the splitting criterion with a maximum depth of 5 levels.

# Dataset Characteristics
Source: Bank marketing campaign data ("bank-full.csv")

Features: 16 customer demographic and behavioral attributes including:

Demographic: age, job, marital status, education

Financial: balance, housing loan, personal loan

Campaign: contact type, duration, previous outcomes

Target Variable: Subscription to term deposit (y)

Data Preprocessing: All categorical variables were encoded using Label Encoding

Model Performance Analysis
Strengths:
High Overall Accuracy: 88.48% indicates good predictive capability

Excellent Performance on Majority Class:

Precision: 90% | Recall: 97% | F1-score: 94% for "no subscription"

Correctly identifies most customers who won't subscribe

# Critical Limitations:
Severe Class Imbalance Issue:

Majority class ("no"): 7,952 instances (87.9%)

Minority class ("yes"): 1,091 instances (12.1%)

Poor Minority Class Performance:

Precision: 55% | Recall: Only 23% | F1-score: 33% for "subscription"

Misses 77% of actual subscribers - major business impact

# Key Business Insights from Decision Tree Primary Decision Drivers:
Call Duration: Likely the most important split - longer calls correlate with higher subscription

Previous Campaign Success: Customers with positive outcomes in past campaigns

Contact Timing: Specific months showing higher conversion rates

Customer History: Previous contact frequency and outcomes

# Customer Segmentation Patterns:
The tree reveals specific customer profiles most likely to subscribe

Combinations of duration thresholds with historical campaign data create targeted segments

Certain demographic clusters emerge as more responsive

Business Implications
Positive Impact:
Efficiently identifies 97% of non-subscribers, saving resources

Provides clear rules for customer targeting

Visual tree enables easy interpretation by non-technical stakeholders

# Critical Business Risk:
Missing 77% of potential subscribers means significant revenue loss

Marketing budget wasted on ineffective targeting

Opportunity cost of not reaching convertible customers

# Recommendations for Improvement Immediate Actions:
Address Class Imbalance:

Use class_weight='balanced' in Decision Tree

Implement SMOTE for oversampling minority class

Try ensemble methods like Random Forest

Model Enhancement:

Experiment with different max_depth values

Try cost-sensitive learning

Use precision-recall curve for evaluation instead of accuracy

Strategic Recommendations:
Focus on Recall Improvement for subscription class

Combine with Business Rules for high-value segments

Implement Tiered Approach: Use model for initial screening + manual review for borderline cases

Continuous Monitoring of actual campaign results vs predictions

Conclusion
While the model demonstrates good technical accuracy, its poor recall for subscribers (23%) makes it commercially suboptimal. The decision tree provides valuable insights into customer behavior patterns but requires immediate attention to class imbalance to become a reliable business tool. The visual nature of the tree offers excellent explainability for marketing teams to understand the "why" behind predictions.
