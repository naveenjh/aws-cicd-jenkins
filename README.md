# aws-cicd-jenkins
This repository is for setting up Jenkins for in AWS Ec2 instance for Continuous Integration and Continuous Deployment.
Prerequisite:
1.create iam policy (permission) "minimum Sec Model" with Ec2, cloudwatch and S3 access only.
2.create a group and attach this policy to that group 
3.create a user and give permissions by attaching it to group while creation.
you can also directly attach the policy to user. Download user access key and secret access key which is required to connect to aws from aws cli
4.create ec2 machine using this user so that user has the minimum permission required to perform the tasks.
