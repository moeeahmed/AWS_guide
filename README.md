# AWS guide
##Setting up remote connection with VS Code
1. Install the Remote SSH Extension in VS Code
2. Click on the status item in the bottom left corner and open The Configuration file
3. Enter the following details:
        
        Host aws-ec2
          HostName ec2-44-229-243-8.us-west-2.compute.amazonaws.com
          User ubuntu
          IdentityFile ~/aws-key/test-key-pair.pem
    

