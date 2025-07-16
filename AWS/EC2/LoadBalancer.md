## use this script for path based routing
````
#!/bin/bash
sudo -i
yum install httpd -y
systemctl start httpd 
systemctl enable httpd 
echo "This is Home Page" > /var/www/html/index.html
cd /var/www/html/
mkdir mobile laptop
echo "This is mobile page" > /var/www/html/mobile/index.html
echo "This is laptop page" > /var/www/html/laptop/index.html
````
