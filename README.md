Public IPv4 address = 3.249.104.197
Public IPv4 DNS = ec2-3-249-104-197.eu-west-1.compute.amazonaws.com

Project Documentation: Landing Page Deployment
This document outlines the steps involved in provisioning a server, installing a web server, deploying an HTML page, and configuring networking for a simple landing page project.

1. Server Provisioning:

Launch an EC2 Instance:

Log in to the AWS Management Console.
Navigate to the EC2 service.
Launch a new instance, selecting an Amazon Linux 2 AMI and a t2.micro instance type (or equivalent free tier option).
Create a new security group and allow inbound traffic on port 80 (TCP) for HTTP access. This allows incoming requests to the web server.
Launch the instance and wait for it to enter the "Running" state.
Connect to the Instance:

Obtain the public IP address of the launched instance from the EC2 console.
Use an SSH client (e.g., PuTTY) to connect to the instance using the public IP address and the default username (ec2-user).
2. Web Server Installation:

Update System:

Update the package lists on the instance:

Install Apache:

Install the Apache web server package:

Start and Enable Apache:

Start the Apache service:

3. HTML Page Deployment:

Create the HTML Page:

Create an HTML file named index.html containing the desired content for your landing page.
Transfer the HTML File:

Use the AWS console to connect to your instance using the "Connect" option.
Navigate to the /var/www/html directory using the cd command.
Upload the index.html file using the file upload functionality within the AWS console.


4. pushing to repo
1.Create a GitHub Repository:


2. Create and Add Files

Create your index.html file:
Place your index.html file (with the content of your landing page) within the project directory.
Add and Commit Changes:
Add the files to the staging area:
Bash

git add . 
Commit the changes with a descriptive message:
Bash

git commit -m "Initial commit of landing page"
3. Push to GitHub

Push the changes to the remote repository:
Bash

git push origin main 
(Replace main with your default branch if it's different)
4. Configure GitHub Pages

Go to your repository's settings on GitHub.
Locate the "GitHub Pages" section.
Select "Deploy from a branch."

