### Launch EC2 instance with Amazon-Linux AMI
### Click http check box 
## Connect 
### switch to root user
````
sudo -i
````

### update
````
yum update
````
### Install httpd webserver
````
yum install httpd -y
systemctl start httpd
systemctl enable httpd
````
### check status of httpd server
````
systemctl status httpd
````

### create index.html in /var/www/html/ dir
````
echo "Hello World" > /var/www/html/index.html
````
### Access web page on your terminal and browser
- for terminal
````
curl localhost
````
![image](https://github.com/user-attachments/assets/dcdcd391-e8f4-4822-9acf-3103ffbd5d6d)

- copy instance public ip address and paste it to browser

![image](https://github.com/user-attachments/assets/b6db883c-3d82-4687-af57-64f786a3f22d)

---
# TO Host Static Website follow these steps:
**note:** our website template is stored on git so first we need to install git
````
yum install git -y
````
- now download code from git
````
git clone https://github.com/abhipraydhoble/staticwebsites.git
````
- once code is downloaded
````
cd staticwebsites
````
````
ls
````
- you will find multiple dir's, choose any one
````
cd yoga
````
- move all data from yoga dir to /var/www/html/ dir

````
mv * /var/www/html/
````

## go to browser refresh the ip 
![image](https://github.com/user-attachments/assets/c93859d9-7bec-4ae9-a991-699f8df1cbf2)
