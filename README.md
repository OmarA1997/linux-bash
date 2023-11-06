# linux-bash
#!/bin/bash
# --------------------------------
# Author: 
# Topic: AWS CLI installation
# Note: run this file with sudo bash filename.sh
# --------------------------------

# REMOVE THE OLD VERSION

# 'which' command directory path
which aws # display aws directory path
sleep 3
ls -l /usr/local/bin/aws # list directory content

sudo rm /usr/local/bin/aws # 
sudo rm /usr/local/bin/aws_completer #

sudo rm -rf /usr/local/aws-cli #
sudo rm -rf ~/.aws/

# check whether removed
ls -l /usr/local/bin/aws 
# Output: No such file or directory 

# INSTALL
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip -u awscliv2.zip
sudo ./aws/install
aws --version 
sleep 3
echo "run 'aws help' for more info"
#aws help
sleep 3

# CONFIGURE AWS 
aws configure 
# use lab credentials from details button
