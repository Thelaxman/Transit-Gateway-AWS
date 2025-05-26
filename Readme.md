# Transit-Gateway
Transit gateway is a network hub that allows you to connect to multiple VPCs, on-prem networks, and other AWS services through a single gateway.

# Why to use Transit Gateway when we already have VPC peering?
VPC peering has a major drawback that is creating one to one peering connection between multiple VPCs in order for the instances to peer with each other. Transit Gateway resolves this issues by acting as a central hub that connects multiple VPCs and on-prem networks using a single gateway. Hence, solving the issue of scaling the network.


## Prerequisites
- IAM role with access to EC2 instances and networks.
- VPCs
- EC2 instances
- TGW Protocol
- Route Table
- Security Groups
- Access to multiple regions

### Setup Instructions
- [Step 1:Create a VPC in different region(atleast 2).](VPC.md)
- [Step 2:Launch multiple instances using the public subnets in those regions.](EC2.md)
- [Step 3:Create a Transit Gateway in each region that you want to peer.](transit-gateway.md)
- Step 4:Create a Transit Gateway attachment using the Transit Gateway created earlier in each region that you want to peer.
- Step 5:Configure Routing Table of each region to route the traffic to VPC in the other regions.
- Step 6:Create a Transit Gateway peering connection from one region to other usin the acceptor Transit Gateway ID, and accept the request from the other region.
- Step 7:Update the static routes to other regions in the Transit Gateway Route Table.
- [Step 8:Connect to the instances and test the connection to other regions by pinging them.](Test-connection.md)
