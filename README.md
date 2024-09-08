# AWS Sagemaker Deployement Guardrail Shadow Testing For Employee Promotion Datatset

## Overview

This repository presents the analysis and prediction of employee promotions using ML algorithms. The goal is to explore and compare the performance of these two models in predicting which employees are likely to be promoted based on various features, while deploying it on AWS Sagemaker and then prforming shadow testing.

## Dataset

The dataset used for this analysis is included in the 'data' directory. It contains relevant features such as employee performance metrics, tenure, education level, and more. The dataset is named `Employees Promotion.csv`.

Objective: Implement guardrails and shadow testing in Amazon SageMaker to ensure model safety, reliability, and performance before deployment.
Guardrails: Predefined checks to catch anomalies, data drift, model bias, and other failures.
Shadow Testing: Running new models in parallel to production models to compare their performance without impacting users.

## Key Components
Amazon SageMaker: Managed service for building, training, and deploying machine learning models.
Guardrails: Custom metrics, constraints, and error thresholds applied to monitor the health of models during training and inference.
Shadow Testing: Compare the performance of new models (shadow) to the live production models by routing real traffic to both.

## Project Workflow
Data Collection & Preprocessing: Prepare datasets and ensure data integrity using preprocessing steps.
Model Development: Train multiple machine learning models on SageMaker.
Establish Guardrails:
Monitor input data for anomalies and drift.
Set thresholds for model bias, fairness, and performance.
Create alerts for significant deviations.

## Set Up Shadow Testing:
Deploy a new model (shadow model) in parallel to the current production model.
Route a portion of the traffic to both models.
Compare outputs to evaluate performance.
Metrics Monitoring: Use CloudWatch or SageMaker logs to capture model performance metrics.

## Evaluation:
Analyze data from shadow testing (accuracy, latency, bias).
Adjust models based on insights.

## Expected Outcomes
Improved Model Reliability: Ensure that only models meeting quality thresholds are deployed.
Bias and Fairness Checks: Detect and mitigate any potential bias in predictions.
Continuous Monitoring: Ongoing model health checks through guardrails.
Risk-Free Deployment: Safely test new models without affecting user experience through shadow testing.

## Tools & Technologies
Amazon SageMaker: Model training, deployment, and management.
Amazon CloudWatch: Monitor metrics and set alerts for issues.
Amazon SNS (Simple Notification Service): For alerting based on guardrail violations.
AWS Lambda: For automation around guardrail triggers and actions.

## Acknowledgments
If you have any questions or suggestions, please feel free to open an issue or contact mohammedbilalkhan10@gmail.com.

Happy analyzing and predicting!
