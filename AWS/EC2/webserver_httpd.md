## Launch EC2 instance with Amazon-Linux AMI
## Click http check box 
## Connect 
## switch to root user
````
sudo -i
````

## update
````
yum update
````
## Install httpd webserver
````
yum install httpd -y
systemctl start httpd
systemctl enable httpd
````
## check status of httpd server
````
systemctl status httpd
````

## create index.html in /var/www/html/ dir
````
echo "Hello World" > /var/www/html/index.html
````
## Access web page on your terminal and browser
- for terminal
````
curl localhost
````
- copy instance public ip address and paste it to browser
---
