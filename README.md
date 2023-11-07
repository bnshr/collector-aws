# collector-aws

## Bootstrap script for EC2

```bash
#!/bin/bash
sudo yum update -y
sudo yum install docker -y
sudo usermod -a -G docker ec2-user
id ec2-user
# Reload a Linux user's group assignments to docker w/o logout
newgrp docker
# Enable docker service at AMI boot time
sudo systemctl enable docker.service
# Start docker service 
sudo systemctl start docker.service
```
