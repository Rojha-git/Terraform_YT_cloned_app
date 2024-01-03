Step-by-Step Guide
1.create an ec2(t2.micro) instance on AWS and after ssh to this instance install terraform on that using below commands: #Confirm the latest version number on the terraform website: https://www.terraform.io/downloads.html

$ wget https://releases.hashicorp.com/terraform/1.0.7/terraform_1.0.7_linux_amd64.zip

$ unzip terraform_1.0.7_linux_amd64.zip

$ sudo mv terraform /usr/local/bin/

$ terraform --version
clone the git repo for terraform scripts:

$ git clone https://github.com/Rojha-git/Terraform_YT_cloned_app.git

$ cd Terraform_YT_cloned_app #under this we have two repo so choose one by one and run below command.

$ terraform init # aws should be configure with your instances

$ terraform plan

$ terraform apply

check the status of the installed services:

check jenkins http://<ip_addr_jenkins_server>:8080

check sonar http://<ip_addr_jenkins_server>:9000

check prometheus http://<ip_addr_monitoring_server>:9090 #if url is not came up check status of service if not running start it using

$ sudo systemctl start prometheus

check grafana http://<ip_addr_monitoring_server>:3000

--Commands to check services

$ sudo systemctl status prometheus

$ sudo systemctl status node_exporter

$ sudo systemctl status grafana-server

