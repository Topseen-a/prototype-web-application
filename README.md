# prototype-web-application

This repository contains the documentation and setup instructions for hosting a web page on a Linux-based virtual machine.

## Public IP Address
- **Public IP Address**: `http://52.207.236.251/`
- This is the IP you can use to access the web page from a browser.

## Screenshots
- The  screenshot of the html page has been added in the images folder

## Provisioning the Server
- I logged in to AWS Management Console
- Launched an EC2 Instance
- I entered a name for my instance, selected a Linux AMI (Amazon Machine Image), Ubuntu Server 22.04 LTS.
- I chose t2.micro (free tier eligible)
- I created a key pair to ssh into the instance
- And then I connected to the instance using ssh to log into the server

## Installing the web server
- In this case, I installed Apache as the web server using various commands like:
- sudo apt install apache2 -y
- sudo systemctl start apache2
- sudo systemctl enable apache2.
- After installation, I opened a web browser and entered the VM's internal IP address

## Deploying the html page
- I created a simple html file using:
- sudo nano /var/www/html/index.html
- saved and exited nano, set proper permissions to ensure that the web server has access to it
- I verified the deployment by opening a web browser and visiting the internal IP address of my server

## Configuring the network
- To make the web page accessible externally, I needed to configure a new Security Group with HTTP (port 80) and SSH (port 22) rules