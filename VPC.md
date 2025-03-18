# Creating and configuring the VPC
VPC(virtual private cloud) is a logically isolated network that allows you to launch EC2 instances in a public or private subnets.


## Create multiple VPC in different regions and name them accordingly. On AWS, choose VPC and more option to select the subnets as well.
- Choose Atleast one AZ(availability zone)
- Select public subnets if you want to make your servers accesible to public.
- If selecting private subnet, then choose NAT Gateway option so you can configure your private IP to public IP from NAT pool to communicate with servers across the web.
- Configure the security groups for your VPC to allow required Inbound and Outbound traffic.
  - Copy the VPC ID and paste it to the Security Groups searchbar -> Select the VPC -> Edit Inbound rules.
  - Select the type of traffic -> SSH, ICMP, and so on.
  - Make sure you select your IP as well to access the servers.

