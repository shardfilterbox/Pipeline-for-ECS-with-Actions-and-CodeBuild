# Pipeline-for-ECS-with-Actions-and-CodeBuild
CI/CD Pipeline for ECS Applications with GitHub Actions and AWS CodeBuild
https://aws.amazon.com/blogs/containers/create-a-ci-cd-pipeline-for-amazon-ecs-with-github-actions-and-aws-codebuild-tests/

Created GitHub Repo
- app.py, a simple Flask web app
- app_test.py, a unit test file
- yml, to instruct CodeBuild to run unit test
- dockerfile, for building the container image
- json, ECS task definition