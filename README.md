# Dev-Project

# Dev-Project

1-Build AWS EC2 Instance:
  _______________________
cd Terraform-Ubuntu-EC2/

terraform init

terraform plan

terraform apply

2-Install Jenkins and other dependencies:
  _______________________________________
vim install.sh

chmod +x install.sh 

./install.sh

3-Setup Jenkins:
 ________________
# Access Jenkins using the EC2 IPv4-Public-DNS:8080

4-Add Github and Dockerhub credentials in Jenkins:
  ________________________________________________
Manage Jenkins > Manage Credentials > Global > Add Credentials

Make sure to use Dockerhub access token instaed of the password Dockerhub > Account Settings > Security > New Access Token

5-Create Jenkins Pipeline:
  ________________________
Choose pipeline, if not found you can install it from Manage Jenkins > Manage Plugins

In Pipeline Section in the end of the page choose Pipeline script from SCM > Add Gihub Repository link > Using Github Credentials

Make usre you choose the right branch and the right path of the Jenkinsfile
