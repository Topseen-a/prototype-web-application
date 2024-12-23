# prototype-web-application

This repository contains the documentation and setup instructions for hosting a web page on a Linux-based virtual machine.

## Public IP Address
- **Public IP Address**: `http://102.89.22.202/`
- This is the IP you can use to access the web page from a browser.

## Screenshots
- The  screenshot of the html page has been added in the images folder

## Provisioning the Server
- I used VirtualBox to create a virtual machine, I chose Ubuntu 22.04 LTS for this setup. I created 
a new vm, allocated resources such as CPU, memory, and disk space. I chose 2 GB of RAM and 20 GB of disk space.

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
- To make the web page accessible externally, I needed to configure port forwarding on my router to allow traffic on port 80 (HTTP) to reach my server.
- I created a port forwarding rule as follows:
External Port (or Src. Port): Set to 80 (for HTTP).
Internal Port (or Dest. Port): Set to 80 (to match the web server's port).
Internal IP Address: 10.0.2.15
- I also configured the Firewall on the Server to ensure the firewall on my VM allows traffic on port 80 (HTTP)
