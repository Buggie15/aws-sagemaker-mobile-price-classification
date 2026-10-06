# Mobile Price Classification using AWS SageMaker & Scikit-Learn

This project demonstrates an end-to-end Machine Learning pipeline built on AWS SageMaker using custom Scikit-Learn scripts.

## Project Architecture
1. **Data Ingestion & S3 Storage**: Processed dataset split and uploaded to AWS S3 using `boto3` and `sagemaker.Session`.
2. **Model Training**: Trained a `RandomForestClassifier` on AWS compute instances (`ml.m5.large`) via SageMaker `SKLearn` Estimator.
3. **Model Artifacts**: Exported `model.joblib` to S3 for reproducibility.
4. **Endpoint Deployment**: Deployed a real-time SageMaker endpoint for live predictions and inference.

## Tech Stack
- **Cloud**: AWS SageMaker, S3, IAM, CloudWatch
- **Languages & Frameworks**: Python 3.12, Scikit-Learn, Pandas, Boto3
- **Dev Environment**: VS Code / GitHub Codespaces

## Results
- **Test Accuracy**: ~88% on held-out test dataset across 4 mobile price tiers.
