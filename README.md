# How do I deploy AWS Lambda using Terraform?

In this, we are working on:
- aws_iam_role
- aws_iam_policy
- aws_iam_role_policy_attachment
- data "archive_file" 
- aws_lambda_function


## aws_iam_role: 
- This resource creates an AWS Identity and Access Management (IAM) role.
- An IAM role is an AWS identity with permission policies that determine what the identity can and cannot do in AWS.

## aws_iam_policy:
- This resource creates an AWS IAM policy.
- An IAM policy is an object in AWS that, when associated with an identity or resource, defines their permissions.
- An AWS IAM policy is a JSON document that defines permissions for users, groups, and roles within your AWS account. It dictates what actions these identities can perform on AWS resources.

## aws_iam_role_policy_attachment
- This resource attaches an IAM policy to an IAM role.
- It acts as a link between the IAM role (which the Lambda assumes) and the IAM policy (which defines permissions).
- Without this attachment, the IAM role would exist but wouldn't have any associated permissions.

## data "archive_file"
- This data source generates a ZIP archive from the specified source. 
- It's used here to package your Python code into a .zip file, which is the required format for uploading to AWS Lambda. 

## aws_lambda_function
- This resource creates an AWS Lambda function. 
- This is the core resource that defines your serverless function, including its code, execution role, runtime, and handler information.

```bash
terraform init
terraform plan
terraform apply
```
