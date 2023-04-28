# AWS Guide

A guide that contains the most important information need to set up and manage your resources on Amazon Web Services (AWS)

## Table of Contents

- [Setting up an SSH connection with EC2 Instance](#setting-up-an-ssh-connection-with-ec2-instance)
- [Setting up remote connection with VS Code](#setting-up-remote-connection-with-vs-code)
***
## Setting up an SSH connection with EC2 Instance

1. Launch EC2 instance on the AWS Console.
2. Choose the AMI (Amazon Machine Image) you want to use.
3. Select the instance type and configure your instance settings.
4. Create or select an existing key pair and download the private key file to your local machine.

To connect via SSH to local machine:

1. Open a terminal or command prompt on your local machine.
2. Navigate to the directory where you saved your private key file.
3. Change the permissions of the private key file using the command: `chmod 400 keyname.pem`
4. Connect to the instance using the command: `ssh -i keyname.pem ec2-user@public-dns-name`

To install packages and carry out updates:

- To update packages install on the instance, use the command: `sudo yum update -y`
- To install packages use the command: `sudo yum install -y`
***
## Setting up remote connection with VS Code

1. Install the Remote SSH Extension in VS Code.
2. Click on the status item in the bottom left corner and open The Configuration file.
3. Enter the following details:

```
Host aws-ec2
  HostName *<server’s host>*.compute.amazonaws.com
  User *<username>*
  IdentityFile *<is the path to the private key>*
```
4. Save the configuration file. 
5. Click on the status item in the bottom left corner and select Connect to Host   
6. Choose your os
7. Now you should be remotely connects to your EC2 instance via SSH
