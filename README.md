# Demo .NET Core Web API CI/CD Pipeline ReadMe

AWS Cloud Formation templates for building a CI/CD Pipeline

## References
- Reference Architecture Repository:  
https://github.com/awslabs/ecs-refarch-continuous-deployment
- Reference Architecture Walk-Through:  
https://docs.aws.amazon.com/AWSGettingStartedContinuousDeliveryPipeline/latest/GettingStarted/ECS_CD_Pipeline.html

## Steps
1. Generate a **Personal Access Token** in GitHub.
    - Go to https://github.com/settings/tokens
    - Click **Generate New Token**
    - Description: AWS CloudFormation Access Token
    - Scopes: repo
    - Click **Generate Token**
    - Copy token to a text file
2. Create S3 Bucket with CloudFormation templates.
    - Go to https://s3.console.aws.amazon.com
    - Click **Create bucket**
    - Bucket name: demo-netcore-api-cicd
    - Region: EU (Ireland)
3. Create CloudFormation Stack.
    - Go to https://eu-west-1.console.aws.amazon.com/cloudformation
    - Click **Create Stack**
    - S3 Template URL:  
      http://demo-netcore-api-cicd.s3-eu-west-1.amazonaws.com/demo-netcore-api-cicd.yaml
    - Stack name: demo-netcore-api-cicd
    - Repo: demo-netcore-api-cicd
    - User name: hilti-labs
    - Personal Access token: Copied from Step 1

