For Testing different models for summarization AWS Sagemaker was used.

Here is the instruction of how this notebooks could be used.

1. You need an AWS account
2. Create AWS IAM Role with necessary permissions for Sagemaker and other required services.
    - Create a new IAM role with the following policies attached:
        * AmazonSageMakerFullAccess (for SageMaker functionality)
        * AmazonS3ReadOnlyAccess (if the notebook uses S3 data)
3. Open AWS Sagemaker, create notebook instance, Attach the IAM role to their SageMaker notebook instance. This allows the notebook to access AWS services with the necessary permissions.
4. Run this instance, open jupyterlab or base UI for jupyter notebooks, upload all the notebooks from AWS folder.
5. Now you can open them and play with it.
6. Don't forget to stop the notebook instance, when you finish the work.