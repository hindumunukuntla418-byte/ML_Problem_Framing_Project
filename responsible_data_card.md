# Responsible Data Card

## Dataset Name

Student Academic Support Dataset

## Purpose

This dataset is used for an educational machine-learning project to study whether a model can help identify students who may benefit from academic-support review.

The model is intended to provide a signal for an academic advisor. It must not be used to automatically punish, reject, fail, or deny opportunities to students.

## Dataset Provenance

The dataset is synthetic and was created specifically for this educational project.

It does not represent real students and does not contain real student records.

## Unit of Observation

One row represents one student at one defined academic assessment point.

## Target Variable

Support_Needed

0 = Student is not flagged for support review.

1 = Student is flagged for support review.

## Input Features

The model uses:

* Attendance
* Previous_Marks
* Study_Hours
* Assignments

Student_ID is not used as a prediction feature.

## Sensitive Attributes

No sensitive personal attributes were intentionally included in the synthetic dataset.

In a real educational dataset, sensitive attributes and protected characteristics would require careful privacy, legal, and ethical review.

## Missing Values

The dataset was checked for missing values.

The current synthetic dataset contains no missing values.

## Duplicate Records

The dataset was checked for duplicate rows.

No duplicate rows were found in the current synthetic dataset.

## Data Leakage Risks

Information that would only become available after the decision point must not be used to make the prediction.

Examples include:

* Final examination results
* Future attendance
* Support received after the prediction date
* Final semester results

## Dataset Limitations

The dataset is very small and synthetic.

It should not be treated as representative of real students or a real educational institution.

The model's performance on this dataset cannot be assumed to represent performance on real-world data.

## Intended Use

The model may be used as an experimental decision-support tool to help an academic advisor identify students who may benefit from further review.

## Unsafe Use

The model should not be used to:

* Automatically fail students
* Automatically reject students
* Punish students
* Deny scholarships or opportunities
* Make final decisions without human review

## Human Oversight

A qualified academic advisor should review any student flagged by the model.

The advisor should consider additional context and should be able to disagree with the model's recommendation.

## Abstention

If the model is uncertain or the input data is incomplete or unreliable, the system should abstain from making a recommendation and send the case for manual review.

## Monitoring

The model should be monitored regularly for:

* Changes in prediction performance
* Increasing false negatives
* Increasing false positives
* Changes in input data
* Missing or incorrect data
* Unexpected prediction patterns

## Rollback Conditions

The model should be removed from use if:

* Serious data leakage is discovered
* Input data becomes unreliable
* Performance becomes unacceptable
* A significant privacy problem is discovered
* The model behaves unexpectedly
* Human reviewers identify unsafe decisions

## Responsible AI Summary

The model is intended only as a decision-support signal.

Human review, privacy protection, monitoring, and the ability to stop or roll back the system are required before considering real-world use.
