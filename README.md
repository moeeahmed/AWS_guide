# AWS guide

##Setting up an SSH connection with EC2 Instance
1. 


##Setting up remote connection with VS Code
1. Install the Remote SSH Extension in VS Code
2. Click on the status item in the bottom left corner and open The Configuration file
3. Enter the following details:
        
        Host aws-ec2
          HostName *<server’s host>*.compute.amazonaws.com
          User *<username>*
          IdentityFile *<is the path to the private key>*
4. Save the configuration file. 
5. Click on the status item in the bottom left corner and select Connect to Host   
6. Choose your os
7. Now you should be remotely connects to your EC2 instance via SSH
