# Project Summary

## Project Title

ML Problem Framing & Responsible Data Card

## Objective

The objective of this project is to demonstrate how a machine-learning problem should be defined and evaluated responsibly before considering real-world deployment.

## Problem

The project explores whether machine learning can help identify students who may benefit from academic-support review.

The model provides a signal for an academic advisor. It does not make the final decision.

## Dataset

A small synthetic student dataset was used for this educational project.

The dataset contains:

* Attendance
* Previous Marks
* Study Hours
* Assignments
* Support Needed

There are 40 student records.

## Baseline

A simple rule-based baseline was created:

* Flag a student if Attendance is below 65
* OR Previous Marks are below 50

The baseline provides a reference point for evaluating the ML model.

## Machine Learning Model

Logistic Regression was used as the candidate machine-learning model.

The model uses:

* Attendance
* Previous Marks
* Study Hours
* Assignments

Student ID was not used as a prediction feature.

## Evaluation

The baseline and ML model were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

## Responsible AI Considerations

The project considers:

* Data provenance
* Missing values
* Duplicate records
* Data leakage
* False positives
* False negatives
* Human review
* Model abstention
* Monitoring
* Rollback conditions
* Privacy risks

## Human Oversight

The model should only provide decision support.

An academic advisor should review flagged cases before any support action is taken.

## Limitations

The dataset is small and synthetic.

Therefore, the results are for educational purposes and should not be treated as evidence that the model is ready for real-world deployment.

## Project Deliverables

The project contains:

1. Problem framing memo
2. Responsible data card
3. Baseline and ML notebook
4. Risk register
5. README
6. Project summary

## Tools

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* VS Code
