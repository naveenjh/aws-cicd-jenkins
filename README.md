# aws-cicd-jenkins
This repository is for setting up Jenkins for in AWS Ec2 instance for Continuous Integration and Continuous Deployment.
Prerequisite:
1.create iam policy (permission) "minimum Sec Model" with Ec2, cloudwatch and S3 access only.
2.create a group and attach this policy to that group 
3.create a user and give permissions by attaching it to group while creation.
you can also directly attach the policy to user. Download user access key and secret access key which is required to connect to aws from aws cli
4.create ec2 machine using this user so that user has the minimum permission required to perform the tasks.
5.login to ec2 instance and run below command to install jdk based jenkins which runs on 8080
`sudo apt-get update
sudo apt install -y default-jdk
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install -y jenkins`
6.password is placed at `sudo cat /var/lib/jenkins/secrets/initialAdminPassword`
7. install the Blue Ocean Plugin into Jenkins.Blue Ocean essentially provides a re-skinned interface for working with Jenkins.. manage plugins-->available-->search blue ocean and install as per blue-ocean-img
8.create pipeline using blue ocean, it will ask for token which you can create by following the wizard on jenkins
9.chose repository on jenking wizard to create the pipeline