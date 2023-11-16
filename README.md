# ML-Workflow-for-Scones-Unlimited

## Overview
This project focuses on building the entire end-to-end workflow for deploying and monitoring an image classification model for a company Scones Unlimited using Amazon SageMaker.

## Getting Started

### Project Files
* **starter.ipynb**: Jupyter notebook showcasing the end-to-end ML workflow, including preprocessing, model training, deployment, and monitoring.
* **lambda-functions**: A folder compiling the scripts for three AWS Lambda functions in the Step Functions workflow.
* **screencaps**: A folder compiling the screen captures of the working Step Function.
* **Step-Function**.json: Step Function exported to JSON.

## Dependencies
* Python 3 (Data Science) - kernel
* ml.t3.medium instance
* Python 3.11 runtime for AWS Lambda Functions

## Installation
For local development, set up a Jupyter Lab instance using the provided instructions. Use Python virtual environments or Docker containers containing Jupyter Lab.

## Approach
The project focuses on developing an image classification ML model using Amazon SageMaker workflows, leveraging AWS Step Functions and Lambda functions for automation.

### Individual AWS Lambda Functions
1. **serializeImageData Lambda Function**: Takes the S3 image address and returns a serialized JSON object.
2. **Classification Lambda Function**: Accepts the JSON object, sends it to an endpoint, and collects inferences as a JSON object.
3. **filter Lambda Function**: Filters low-confidence inferences based on a predefined threshold.

A state machine is built using AWS step functions to test and monitor the workflow.

## Conclusion
This project successfully implements an end-to-end ML workflow, utilizing technologies such as Amazon SageMaker, AWS Step Functions, Lambda functions, and S3 for efficient image classification, deployment, and monitoring for Scones Unlimited.

### Source
This was the final project of the Machine Learning Fundamentals Nanodegree on Udacity as part of the advanced phase of the AWS AI & ML scholarship program in 2023.
