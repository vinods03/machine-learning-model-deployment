# machine-learning-model-deployment

Below machine learning model deployment strategies are covered in deployment.ipynb.
Note that we are using AWS Sagemaker for the model development and deployment.

1. Real-time inference - for low latency predictions.
2. Serverless inference - for unpredictable, fluctuating traffic. Helps to save cost.
3. Batch Transform - for processing very large datasets without needing a constant endpoint. Can be time-consuming and cannot be used for real-time inference requirements.
4. Asynchronous inference - for processing very large datasets, similar to batch transform. Difference is, there is a constant endpoint and also results are not returned to the user but stored in an S3 bucket from where further processing can take place.
5. Multi-model endpoint - one endpoint can host multiple models - cost-effective solution for managing multiple models

Also, note that a model can be deployed using an estimator (of type sagemaker.base_predictor.Predictor) built/trained using pre-built containers and custom data or using a pre-built/pre-trained model tar file.
