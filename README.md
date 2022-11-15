﻿### A simple Terraform Infrastructure which will install an EC2 with all its necessities and run a user data template.
 <hr>
 
 #### Configured to run within us-east-1 (See providers.tf)
 ##### _Credentials key file is set within ~/.aws/credentials - Please create or use a different approach._

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

* This project serves no purpose but hands on.
  
  
