# AWS-RDS-connect-to-EC2
RDS also known as relational database is an aws database service is amanaged sql database service provided by amazon. 
# Create EC2 instance
It will be easy to connect rds to an instance when you have your instance already created. After creating your instance. Let us head to creating the rds
# Create AWS RDS
Search for rds on the search dashboard  
Click on create database  
Select the standard create under the database create method  

Select the standard create under the database create method
Choose mysql in the engine option
Choose free-tier if you are just practicing. Choose production if you want to use it for production.
Give the database identifier name
Let master remain as admin
Choose you master password. 
Click on create database
# Connecting RDS with EC2 instance
Click on the radio button beside the database created
Click on action
Click on set up EC2 connection. This will take you to set up ec2 interface
Select the created instance. The VPC and the security group is added
Click on comfirm and Set up
# Connecting the DB to the instance
SSh into the EC2 instance
Update the instance first by typing sudo apt update
Create this install.sh file and paste the code inside it 
Give the file executable permission by typing chmod u+x install.sh
Executive the file by typing ./install.sh
This helped to install the database into the instance
Paste this code to connect with mysql instance
mysql -h endpoint -p 3306 -u admin -p 
Replace the end point with the endpoint on the created rds on aws console
We have now succesfully connected our RDS database to EC2 instance. 
