# launch-ec2-and-connect-via-ssh
I successfully launched an EC2 instance in AWS using a Windows Amazon Machine Image (AMI).
![Alt text](https://github.com/Naveen15github/launch-ec2-and-connect-via-ssh/blob/bec4f45197d6eb71d9e5974c677ab9cf5864e537/Screenshot%20(100).png)

![Alt text](https://github.com/Naveen15github/launch-ec2-and-connect-via-ssh/blob/bec4f45197d6eb71d9e5974c677ab9cf5864e537/Screenshot%20(101).png)

During the setup, I used my existing key pair (ec2keypair) for secure authentication instead of creating a new one.

I configured the instance inside my custom VPC, selected the public subnet, and enabled auto-assign public IP to allow internet access.
I also created and configured a Security Group to allow SSH (port 22) traffic only from my IP address for secure remote access.
![Alt text](https://github.com/Naveen15github/launch-ec2-and-connect-via-ssh/blob/bec4f45197d6eb71d9e5974c677ab9cf5864e537/Screenshot%20(102).png)

After launching the instance and confirming its running state, I connected to it via SSH using Command Prompt on my local Windows system with the following command:

ssh -i "ec2keypair.pem" administrator@Public-IP-Address


The SSH connection was successful, and I verified it using commands like:

hostname
whoami
ipconfig
