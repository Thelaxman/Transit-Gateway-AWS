
# Creating and configuring the Transit Gateway

A Transit Gateway is a network transit hub that you can use to interconnect your VPCs and on-premises networks. It acts as a central hub to route traffic between multiple VPCs and regions.

## Step 1: Create Transit Gateway in Multiple Regions
- Navigate to the AWS Management Console and select the first region.
- Go to the VPC Dashboard and select **Transit Gateways** from the left-hand menu.
- Click on **Create Transit Gateway**.
- Provide a name and description for your Transit Gateway.
- Set the ASN (Autonomous System Number) as needed or leave the default.
- Configure options such as DNS support and VPN ECMP support as required.
- Click **Create Transit Gateway**.
- Repeat these steps in the second region to create another Transit Gateway.

## Step 2: Create Transit Gateway Attachment
- Go to the Transit Gateway console.
- Select the Transit Gateway you created and click on **Create Attachment**.
- Choose **VPC** as the attachment type.
- Select the VPC from the drop-down list and choose the specific subnets to attach.
- Click **Create Attachment** and wait for the status to become **Available**.

## Step 3: Update Route Tables
- Navigate to the **Route Tables** section within your VPC.
- Select the route table associated with the VPC you attached.
- Edit routes and add a new route with the destination CIDR block of the remote VPC.
- Select **Transit Gateway** as the target and choose your Transit Gateway.
- Save changes.
- Repeat these steps in the second region to update the route table.

## Step 4: Send Transit Gateway Peering Request
- Navigate to the **Transit Gateway Peering** section.
- Click **Create Peering Attachment**.
- Select the local and remote Transit Gateways from the drop-down lists.
- Click **Create Peering Attachment** and wait for the request to be sent.
- In the remote region, accept the peering request.

## Step 5: Update Static Routes
- Go to the **Route Tables** in both regions.
- Update the static routes to include the Transit Gateway peering attachment as the target.
- Verify that routes are properly configured to allow inter-region communication.

