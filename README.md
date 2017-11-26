# Deploy Wordpress Application Stack

## Create VPC

    CIDR: 172.16.X.0/24
    - Subnet: 2 Public
            2 Private ( With Internet )
    - Security Group: 
        1. Private Access
        2. Public Access
        
## Create Private Hosted Zone
    - cypaws.local and attach to the you have created earlier. 
    
## Create a jump server in the public zone

## Create RDS
   - Engine: Mysql
   - MultiAZ: False
   - Create db.<private hosted zone> domain name with route53
   - RDS Must be in private zone
   
## Create an AMI with wordpress installed.
   - OS: Amazon AMI or Ubuntu 16.04

## Create instance from you AMI
   - Setup Wordpress with DB details
   
## Create target groups
    - <yourname>-cypaws
    
## Create ALB load balancer
    - <your name>-cypaws

## Add Loadbalancer name in DNS.
    - Create Listner and add target group
    - ALB name - blog.cypaws.com
     
## Auto Scalling
    - Create  Launch Configuration with Custome AMI 
    - Create Autoscale group
    - Scale by request count 
    - Scale by CPU utilisation






    
