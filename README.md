# challenge7
Tech challenge for Ticketek

## Timeline
- 2021-08-27 10:33 AWS password changed
- 2021-08-27 10:40 Documented requirements on my personal notes (core tasks + bonus)
- 2021-08-27 10:41 Coffee
- 2021-08-27 10:50 Getting to know Opserver https://github.com/opserver/Opserver
- 2021-08-27 10:57 Looking at AWS recommendations for the job https://aws.amazon.com/quickstart/architecture/microsoft-iis/
- 2021-08-27 11:02 Carefully reading the documentation https://aws-quickstart.github.io/quickstart-microsoft-iis/

## Infrastructure: what is getting deployed in AWS

| Resource | Count |
| --- | --- |
| VPCs | 1 |
| Elastic IP addresses | 3 |
| AWS IAM security groups | 6 |
| IAM roles | 5 |
| Auto Scaling groups | 2 |
| Application Load Balancers | 1 |
| T2 or T3 instances | 2 |
| M4 or M5 instances | 2 |

- A highly available architecture that spans two Availability Zones,
- A VPC configured with public and private subnets according to AWS best practices, to provide you with your own virtual network on AWS,
- Amazon EventBridge, providing the rules that trigger automation routines in response to Auto Scaling events,
- AWS Systems Manager to store automation documents,
- AWS Identity and Access Management (IAM) roles,
- Security groups to control traffic to your EC2 instances,
- Amazon Simple Storage Service (Amazon S3) bucket for storing MOP files.

### In the public subnets

- Managed network address translation (NAT) gateways to allow internet access for resources in the private subnets,
- Elastic Load Balancers to distribute traffic across EC2 instances,
- Remote Desktop (RD) gateways in an Auto Scaling group.

### In the private subnets

- Auto Scaling group of EC2 instances into which Microsoft IIS is deployed,
- AWS Directory Service for Microsoft Active Directory.

## Work completed 

