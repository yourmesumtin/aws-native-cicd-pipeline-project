# AWS Native CI/CD Pipeline Project Architecture (Java Web Application)
![CompleteAWSNativeCICDProject!](https://lucid.app/publicSegments/view/798557ac-1687-465b-888b-e7c28207a3c9/image.png)

Copy the contents of this folder and its subfolders to the CodeCommit repo 

# Overview
This repo is a demonstration of Continuous Delivery of a static website to EC2 instances via CodePipeline, CodeCommit, CodeBuild, and CodeDeploy. Ensure you've configured the [Prerequisites](https://github.com/stelligent/devops-essentials/wiki/Prerequisites) before launching the stack below.

# Launch Stack

[![Launch CFN stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/template?stackName=devops-essentials-ec2&templateURL=https://s3.amazonaws.com/www.devopsessentialsaws.com/samples/ec2/pipeline.yml)

# Configure Solution

1. Once the CloudFormation stack is successful, select the checkbox next to the stack and click the **Outputs** tab. 
1. From Outputs, click on the **PipelineUrl** output. The Source action will be in a failed state.
1. From the CodePipeline Source action, click on the CodeCommit provider and copy the **git clone** statement provided by CodeCommit
1. Paste the command in your Terminal
1. Copy **all** of the contents from [this](../ec2) folder to your locally cloned CodeCommit Git repo
1. From your Terminal, type `git add .`
1. From your Terminal, type `git commit -am "add new files"`
1. From your Terminal, type `git push`
1. Go back to your pipeline in CodePipeline and see the changes flow through the pipeline
1. Once the pipeline is complete, go to your CloudFormation Outputs and click on the **CodeDeployURL** Output to get to the EC2 instance for which CodeDeploy has deployed the application


# Project Resources 

1. The CloudFormation template is available [here](https://s3.amazonaws.com/www.devopsessentialsaws.com/samples/ec2/pipeline.yml).
