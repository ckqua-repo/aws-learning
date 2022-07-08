The goal of this first set of YAML templates is to become more comfortable making use of CloudFormations intrinsic functions such as !Ref, !Sub, and !Join, etc. 

I challenged myself to create basic network infrastructure and an Ec2 instance to populate the VPC from memory. However, I referenced documentation when absolutely necessary.

The networking components consist of a VPC, Internet Gateway, Route Table, four Subnets, and 2 Security Groups. I used unconventional names when naming some of the logical resources as a means to break the mental mold of tutorials. 

The EC2 template is a basic t2.micro instance which has a bootstrap script that updates the instance and installs httpd, making it a webserver upon start up. I initially had a creation policy of 20 minutes but the wait condition was causing rollbacks though the update and install didn't take that long.

In the future I will troubleshoot the creation policy in other templates as I progress as a CloudFormation template developer.