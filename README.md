# Transit-Gateway
Transit gateway is a network hub that allows you to connect to multiple VPCs, on-prem networks, and other AWS services through a single gateway.

## Prerequisites
-IAM role with access to EC2 instances and netwroks.
-VPCs
-EC2 instances
-TGW Protocol
-Route Table
-Security Groups
-Access to multiple regions

### Setup Instructions
-Step 1:Creating VPC in different region(atleast 2).
-Step 2:Launching multiple instances using the public subnets in those regions.
