
This Module will create an EC2 Instance in AWS

##USAGE:

provider "aws" {
    region = "ap-south-1"
}

module "ec2-instance" {
    source = "github.com/donpasscall/ec2-module"
    ami_id = "ami-id-of-your-choice"   
    instance_type = "t2.micro"
    vpc_id = "vpc-id-your-choice"   #vpc id of your choice
    port = "your-port-choice"
    cidr_block = "0.0.0.0/0"
}
