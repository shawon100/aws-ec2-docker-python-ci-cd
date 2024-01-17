# aws-ec2-docker-python-ci-cd
Sample Python flask app CI/CD for docker on AWS ec2

```
Install docker and docker compose on your ec2 machine

For Amazon Linux:
yum update -y
amazon-linux-extras install docker
service docker start
usermod -a -G docker ec2-user
chkconfig docker on

For Ubuntu:

sudo apt-get update
sudo apt-get install docker.io
sudo systemctl enable docker 
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker 


Docker Compose:
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

docker-compose version


Configure ecr access on ec2 machine

aws ecr get-login-password --region us-east-2 | docker login --username AWS --password-stdin your-ecr-registry-url

Example:


aws ecr get-login-password --region us-east-2 | docker login --username AWS --password-stdin 32423423423.dkr.ecr.us-east-2.amazonaws.com/ecr-repository

If you have still access problem, attach ecr iam role with your ec2



```

