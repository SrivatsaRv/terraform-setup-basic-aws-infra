## Things I Need to Build This? 
- AWS Cloud Account (Business / Personal)
- IAM User  
- VPC (1 in Region of your Choice)
- Subnets - 2 Subnets (Private and Public in same region)
- EC2 Instances (2x  - t2.micro free tier) 
- Security Groups 
- NAT Gateway (1x per VPC) 
- Internet Gateway (1x per VPC)


## Order of Creation - 
- IAM account - already present
- VPC with config
- Private Public Subnet with Config
- EC With Config
- Internet Gateway with Config
- NAT Gateway with Config 
- SSH Key Pair? - idk


## Architecture Diagram 
![Proposed Architecture](AWS_Setup-BasicTF.png)



## Running thoughts 
- How to install Terraform on Amazon Linux - https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli


## End Goal - How to Verify? 
- You should be able to login into the public-ec2 isntance created , 
- And should be able to effortlessly SSH into the private instance in the private subnet without any issues 
- Both instances should be able to reach the internet gateway , and run their package updates. 
- this will prove the architecture has been deployed as intended, and can be used to deploy re-deploy 


## Future Capabilities , 
- deploy to multi-region
- setup observability with node-exporter on the EC2 when they come up 
- connect with Prometheus instance, and Grafana Cloud
- Public dashboard with Golden Signals 


