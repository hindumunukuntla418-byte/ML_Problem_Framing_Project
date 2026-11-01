# ML Problem Framing & Responsible Data Card

## Project Overview

This project demonstrates how to properly frame a machine-learning problem before training a model.

The project focuses on identifying students who may benefit from academic-support review. The machine-learning model is used only as a decision-support signal. Final decisions require human review.

## Project Goals

The main goals are to:

* Define the ML decision and prediction target
* Establish a non-ML baseline
* Check data quality
* Document data provenance and limitations
* Identify data leakage risks
* Compare baseline and ML performance
* Identify false-positive and false-negative risks
* Define human-review and abstention procedures
* Define monitoring and rollback conditions

## Dataset

The dataset is a small synthetic dataset created for educational purposes.

It contains 40 student records with the following columns:

* Student_ID
* Attendance
* Previous_Marks
* Study_Hours
* Assignments
* Support_Needed

The dataset does not contain real student records.

## ML Problem Definition

### Decision

Whether an academic advisor should review a student for possible additional academic support.

### Prediction Target

`Support_Needed`

* `0` = No support flag
* `1` = Support review

### Unit of Observation

One student at one defined academic assessment point.

### Action Window

A flagged student should be reviewed by an academic advisor within the defined support-review period.

## Non-ML Baseline

The baseline flags a student when:

`Attendance < 65 OR Previous_Marks < 50`

This simple rule is used as a reference point for evaluating the machine-learning model.

## Machine Learning Model

The project uses Logistic Regression.

Features used:

* Attendance
* Previous_Marks
* Study_Hours
* Assignments

`Student_ID` is not used as a prediction feature.

## Evaluation Metrics

The project evaluates:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

Recall is important because false negatives may result in students who could benefit from support not being identified.

Precision is also important because false positives may create unnecessary advisor workload.

## Responsible AI Considerations

The project includes:

* Data provenance
* Missing-value checks
* Duplicate checks
* Sensitive-attribute considerations
* Data leakage risks
* Human oversight
* Abstention
* Monitoring
* Rollback conditions
* Risk register

## Human Oversight

The model must not make automatic decisions about students.

Any flagged case should be reviewed by an academic advisor, who can consider additional information and disagree with the model.

## Limitations

The dataset is small and synthetic.

Therefore, the results are intended only for educational demonstration. They should not be interpreted as evidence that the model is suitable for real-world educational decision-making.

## Project Structure

```text
ML_Problem_Framing_Project
│
├── README.md
│
├── data
│   └── students.csv
│
├── notebooks
│   └── baseline.ipynb
│
├── documents
│   ├── problem_framing_memo.md
│   └── responsible_data_card.md
│
└── risk
    └── risk_register.md
```

## Tools Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* VS Code

## Expected Learning Outcome

This project demonstrates the importance of defining the problem, establishing a baseline, checking data quality, considering risks, and planning human oversight before deploying a machine-learning system.
