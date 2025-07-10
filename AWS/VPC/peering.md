# VPC Peering 

![image](https://github.com/user-attachments/assets/66212546-60ac-4021-893f-4aed05b294fa)


step1: create two vpc's 
 -> VPC-A [192.168.0.0/16]
   > create subnet
   > igw 
   > route table

 -> VPC-B [10.0.0.0/16]
   > create subnet
   > igw 
   > route table

steps2: create security group for vpcA and vpcB
 > SSH
 > ALL ICMP

step3: launch ec2 instances in each vpc 

step4: create peering connection 
 > requester=vpcA 
 > accepter=vpcB 

step5: edit route tables 
-> rt(vpcA) 
    - 10.0.0.0/16(cidr block of vpcB)    and select peering connection

-> rt(vpcB)
    - 192.168.0.0/16(cidr block of vpcA)    and select peering connection


step6: 
-> ping ip of vpcB from vpcA instance and vice versa
