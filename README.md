# Shell-scripting
A shell-script to automate file management in linux system. Which has a feature of identifying files below 20kb and move it to archive folder. But before that it checks either the archive folder is created or not. In case of not, it creates first.

Connecting to EC2 instance with SSH.
We have to create a key pair by which we can connect to our instance remotely.
To connect with ssh follow below command.
ssh -i ./<private-key> ec2-user@<public-ip>
Once connection established, create a directory under EC2 instance. Create a demo file in your local to upload in EC2.

Steps to upload it to EC2 securely.
Use the below command to upload the file.
scp -i ./<private-key> ./<text-file> ec2-user@<public-DNS-name>:<folder-of-ec2>
Uploading completed.

Creating shell-script.
Create a shell-script file in EC2. You can use my shell-script to automating file management on EC2. It identifies files less than 20kb and move it to archive folder. It also creates a archive folder incase it doesn't exist.
Once creation is done, you can give it a run to check if it is working fine.
