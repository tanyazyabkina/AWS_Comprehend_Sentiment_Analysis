# Amazon Comprehend Sentiment Analysis
Sentiment analysis using BOTO3 for Python on Amazon Comprehend

This projects uses BOTO3 package for python.

## What is Amazon Comprehend?
It’s a collection of pre-trained Natural Language Processing models and you can use to analyze your text. 
You can customize some of the models for your particular output types (document classification, entities detection).

## AWS API Setup
Steps:
1. Create an AWS account
2. Create a user that has appropriate permissions (Comprehend, S3)
3. Create and download access keys
4. Use AWS CLI (Command Line Interface) to create environment variabes folder
5. Install BOTO3 package

References:
https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user.html?icmpid=docs_iam_console
https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html

## AWS Comprehend Cost
* Free AWS Tier: Limit 50K units (5M characters) a month, $1 per 10K above.*
1 unit is 100 characters, and every tweet is ~2 units. 
In a scheduled job I am analyzing 1K tweets at once, so the free tier runs out fast. Be sure to check pricing before you proceed.

Reference:
https://aws.amazon.com/comprehend/pricing/

## Data
For my test run I used Twitter data.
You can get my 1,000 tweet and other samples there:
https://github.com/tanyazyabkina/AmazonComprehend

## Three Ways to Run Sentiment Analysis
The notebook shows these three ways to run the analysis.
1. One text document at a time. 
Feed data directly from python, receive results back into python. Real time.
2. A batch of up to 25 documents. 
Feed data directly from python, receive results back into python. Real time.
3. Create an asynchronous Analysis Job.
Feed the data from an S3 bucket. The results are saved into an S3 bucket. More powerful, but a lot more involved.

Reference. 

Boto3 S3: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/comprehend.html  

Boto3 Comprehend: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/s3.html
