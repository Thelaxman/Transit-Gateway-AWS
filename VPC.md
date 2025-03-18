# Creating and configuring the VPC
## Create multiple VPC in different regions and name them accordingly. On AWS, choose VPC and more option to select the subnets as well.
- Choose Atleast one AZ(availability zone)
- Select public subnets if you want to make your servers accesible to public.
- If selecting private subnet, then choose NAT Gateway option so you can configure your private IP to public IP from NAT pool to communicate with servers across the web.
- Configure the security groups for your VPC to allow required inbound and outbound traffic.
  - SSH, ICMP, and so on.
