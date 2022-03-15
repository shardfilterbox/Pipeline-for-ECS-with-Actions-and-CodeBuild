# Pipeline-for-ECS-with-Actions-and-CodeBuild
CI/CD Pipeline for ECS Applications with GitHub Actions and AWS CodeBuild

Services: Github, Amazon ECS, Amazon ECR, AWS CLI and CDK
Languages: Python/Flask
Configs: yml, json, dockerfile



Created GitHub Repo Pipeline-for-ECS-with-Actions-and-CodeBuild
- app.py, a simple Flask web app
- app_test.py, a unit test file
- yml, to instruct CodeBuild to run unit test
- dockerfile, for building the container image
- json, ECS task definition

Created ECS Infrastructure
- Initialize CDK project
- Activate venv
- Install general and ECS dependencies
- Replaced ...stack.py to create ECS infrastructure
    - Creates ECR Repository
    - Creates the ECS Cluster
    - Creates ECS task definitio
        - Runs using a container from public AWS registry
        - Replaced after CI/CD pipeline updates
        - This is so that the Service stabilizes before adding container images
    - Creates ECS service    
- Deployed - AttributeError: partially initialized module 'aws_cdk' has no attribute

Created CoodeBuild Project
- ecs-devops-sandbox
- Connected to Github
- Configured source Pipeline-for-ECS-with-Actions-and-CodeBuild
- Report build statuses to source when builds start and finish
- Rebuild everry code change
- Managed image, Ubuntu, aws/AWS CodeBuild/standard:3.0

Created Github Workflow
- 




https://aws.amazon.com/blogs/containers/create-a-ci-cd-pipeline-for-amazon-ecs-with-github-actions-and-aws-codebuild-tests/