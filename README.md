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
- Step 1:Create a VPC in different region(atleast 2).
- Step 2:Launch multiple instances using the public subnets in those regions.
- Step 3:Create a Transit Gateway in each region that you want to peer.
- Step 4:Create a Transit Gateway attachment using the Transit Gateway created earlier in each region that you want to peer.
- Step 5:Configure Routing Table of each region to route the traffic to VPC in the other regions.
- Step 6:Create a Transit Gateway peering connection from one region to other usin the acceptor Transit Gateway ID, and accept the request from the other region.
- Step 7:Update the static routes to other regions in the Transit Gateway Route Table.
- Step 8:Connect to the instances and test the connection to other regions by pinging them.
