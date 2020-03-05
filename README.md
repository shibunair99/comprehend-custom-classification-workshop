# Comprehend-custom-classification-workshop
AWS Comprehend Custom Classification Workshop
Services Used: SageMaker, Comphrehend, S3 and IAM.

## Background
You can use Amazon Comprehend to build your own models for custom classification. You can also assign a document to a specific class or category, or to multiple ones.

Custom classification is a two-step process. First, you train a custom classifier to recognize the classes that are of interest to you. Then you send unlabeled documents to be classified.

To train the classifier, specify the options you want, and send Amazon Comprehend documents to be used as training material. Based on the options you indicated, Amazon Comprehend creates a custom ML model that it trains based on the documents you provided. This custom model (the classifier) examines each document you submit. It then returns either the specific class that best represents the content (if you're using multi-class mode) or the set of classes that apply to it (if you're using multi-label mode). 
## Prerequisites
###   AWS Account
In order to complete this workshop, you'll need an AWS Account with access to create AWS IAM, S3 and Sagemaker. The code and instructions in this workshop assume only one student is using a given AWS account at a time. If you try sharing an account with another student, you'll run into naming conflicts for certain resources. You can work around these by appending a unique suffix to the resources that fail to create due to conflicts, but the instructions do not provide details on the changes required to make this work.
### Setting up SageMaker notebook
[SageMaker Notebook Setup instructions ]( https://github.com/markproy/sagemaker-workshop/blob/master/lab-0-setup/README.md)

### Main Workshop
Setup 
Note: In order for this workshop to work, the Sagemaker Execution role must have AmazonComprehendFullAccess to create custom classifier and analysis jobs. Also Sagemaker Execution role has CreateRole, AttachRolePolicy and PassRole.

## Contents
[SageMaker Notebook](comprehend-custom%20classification%20workshop.ipynb)
