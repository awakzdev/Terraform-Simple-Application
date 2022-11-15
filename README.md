﻿### A Terraform Infrastructure which will install an EC2 with all its necessities and run a bootstrapped template.
 <hr>
 
 ##### _Credentials key file is set within ~/.aws/credentials - Please create or use a different approach. [refer to documentation](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)_
*Your credentials file should look like this*
 ```
 [default]
# This key identifies your AWS account.
aws_access_key_id = foo
# Treat this secret key like a password. Never share it or store it in source
# control. If your secret key is ever disclosed, immediately use IAM to delete
# the key pair and create a new one.
aws_secret_access_key = foo
 ```
 ##### _SSH Key will need to be created using the following_
 `ssh-keygen -t ed25519` > You'll need to rename it to ec2 otherwise please edit the aws_key_pair resource under main.tf.

## *Its purpose is to serve the following configuration*
```
VPC - Set to support DNS hostnames/support.
Subnet - Set to map a public IP on launch.
Internet Gateway - Allowing outside traffic.
Routing Table / Association (Bridging for subnet).
Security Groups - Set to accept all connections within all protocols.
Key pair - SSH Connectivity.
AMI - Ubuntu 22.04.1 LTS (Jammy Jellyfish).
EC2 Instance - Increased default volume size to 10 and launched a user_data template to install dockerfile.
```

###### *This project serves no purpose but hands on.*
  
  
