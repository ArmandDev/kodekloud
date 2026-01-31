# 100 Days of Cloud (AWS)

1. Create a key pair command: aws ec2 --key-name "Armand_key" --key-type rsa --region "eu-central-1"
2. Create a security group under default VPC:
   - Find vpc id: aws ec2 describe-vpcs 
   - aws ec2 create-security-group --group-name "xfusion-sg" --description "Security group for Nautilus App Servers" --region "us-east-1" --vpc-id "vpc-08539ddce2134a19e"
   - Find security group id: aws ec2 describe-security-groups
   - aws ec2 authorize-security-group-ingress --group-id sg-12345678 --protocol tcp --port 80 --cidr 0.0.0.0/0   
