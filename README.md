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
Attn: Make a note of SageMaker Execution role and S3 bucket you are creating in section.
For step by step instructions to create SageMaker notebook, follow below steps.
[SageMaker Notebook Setup instructions ]( https://github.com/markproy/sagemaker-workshop/blob/master/lab-0-setup/README.md)

Navigate to IAM - https://console.aws.amazon.com/iam/

Follow below steps to Grant CreatePolicy,CreateRole,AttachRolePolicy,PassRole to sagemaker execution role you have created already.

Create Policy

Open the IAM console at https://console.aws.amazon.com/iam

Navigate to Policies and click on 'Create policy', goto "JSON' tab and paste below

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:CreatePolicy",
                "iam:PassRole",
                "iam:CreateRole",
                "iam:AttachRolePolicy"
            ],
            "Resource": [
                "arn:aws:iam::xxxxxxxxxxx:role/*",
                "arn:aws:iam::xxxxxxxxxxxx:policy/*"
            ]
        }
    ]
}
```

Follow direction and create the policy. Keep this policy name handy for next steps.

1. Click on Roles and search for newly created SageMaker execution role by seach the role name by creation date. 

2. Attach new policy created in step 1 to sagemaker execution role.

3. Click on Attach policies and key-in the policy name you have created earlier step in search box near "Filter Policies" and click enter. Once the policy appeared, select the policy and click 'Attach policy' button 

4. Repeat the steps 1 and then search for "ComprehendFullAccess", select it and attach the same to SageMaker execution role


### Main Workshop

[Comprehend Custom Classifier SageMaker Notebook](comprehend-custom%20classification%20workshop.ipynb)

