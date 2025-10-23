I logged in to the AWS Management Console and went to the VPC Dashboard.

I created a new VPC named elevate-labs-day3-vpc with the CIDR block 10.0.0.0/16.

Then, I created two subnets:

Public Subnet → 10.0.1.0/24 (enabled auto-assign public IP)

Private Subnet → 10.0.2.0/24 (disabled auto-assign public IP)

After that, I created an Internet Gateway named elevate-labs-day3-igw and attached it to my VPC.

I created two route tables:

Public Route Table — added route 0.0.0.0/0 → Internet Gateway

Private Route Table — only had local route (10.0.0.0/16)

I associated the public route table with my public subnet and the private route table with my private subnet.

Finally, I checked the VPC Resource Map to verify that everything was connected properly.

 Network Details

VPC Name: elevate-labs-day3-vpc

VPC CIDR: 10.0.0.0/16

Public Subnet CIDR: 10.0.1.0/24

Private Subnet CIDR: 10.0.2.0/24

Region: US East (N. Virginia)

Internet Access: Enabled for public subnet only

Screenshots

VPC Resource Map

Public Route Table

 Result

I successfully created a VPC with both public and private subnets.
The public subnet has internet access through the Internet Gateway, while the private subnet remains isolated.
