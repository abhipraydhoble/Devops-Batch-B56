
## steps to create vpc with igw and nat

#  create vpc 
 -> give name to vpc
 -> give cidr block  (example: 192.168.0.0/16)

# create subnets
 -> select vpc id 
 -> give name to subnet 
 -> select availability zone
 -> give subnet cidr block (example: 192.168.0.0/22)

# create internet gateway
 -> give name 
 -> attach igw to vpc 


# create nat gatway (nat-gw is used to give access of internet for private subnet)
 -> give name 
 -> select public subnet
 -> allocate elastic ip 
 -> create nat 

# create route table for public subnet
 -> give name 
 -> edit subnet association (select public subnet)
 -> edit routes (add internet gateway)

# create route table for private subnet
 -> give name 
 -> edit subnet association (select private subnet)
 - edit routes (add nat-gw)



# now launch instances in respective subnets
 note: 
  a) instance launched in public subnet has public_ip
  b) instance launched in private subnet has no public ip

# how to connect private instance via public instances
 -> as both instances share same network therefore we can access private server via public server
 -> for that we need add key pair in public server
 -> login into public server
 -> there are two ways we can share key pair
  1] scp (example:  scp -i keypair.pem keypair.pem ec2-user@public_ip:/home/ec2-user/)
  2] direct copy content from key and paste it to .pem file in public server
 -> give permission 400 to keypair 
 -> try ssh and connect to private server 
 -> ex.  ssh -i keypair.pem ec2-user@private_ip 
 -> tadaaa congrates! you succesfully logged into private server 
 -> you can also try install something to check nat connectivity
