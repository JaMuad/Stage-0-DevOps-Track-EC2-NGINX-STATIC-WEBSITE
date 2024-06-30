
# AWS EC2 Static Website Project

## Introduction
This project aims to host a static website on AWS using services EC2 and Route 53. The website hosts my resume written in HTML and styled with CSS. 

## Step-by-Step Guide

### 1. Review the Challenge Requirements

Cloud Platform: AWS 

Web Server: NGINX

Static Website: A ready-to-deploy static website project (HTML, CSS, Javascript) which includes Name and Email.

### 3. HTML and CSS
index.html file

### 4. Deploy Static Website on Amazon EC2 Instance
18.209.63.11

### 5. Enable HTTPS with Amazon CloudFront
Using Certbot instead of CloudFront for SSL certification 

### 6. Set Up Custom Domain with Route 53
personal Domain Link: nginx.muadmaalim.buzz

### 7. Document Progress
Step 1: Set Up EC2 instance for Static Website Hosting

Create an  EC2 Instance:

Open the Amazon EC2 console.

Create a new Instance or using Existing Instance.

1) Open EC2 Instance and connect to your Ubuntu EC2  

chmod 400 ~/Downloads/Your-key-on-Download-folder.pem

ssh -i "Your-key-on-Download-folder.pem" ubuntu@ec2-Your-Public-IP.compute-1.amazonaws.com

2) Update the system

sudo apt update && sudo apt upgrade -y

3) Install NGINX

sudo apt install nginx -y

4) Start Nginx

Sudo systemctl start nginx

5) Set Up Route 53  

+Go to the Route 53 service in the AWS Console. 

+Create a hosted zone for your domain

+Update the domain's DNS settings to point to your EC2 instance's public IP address.

6) Obtain and Install SSL Certificates 

sudo apt install certbot python3-certbot-nginx

sudo certbot --nginx -d yourdomain.com -d subdomain.yourdomain.com

7) Restart Nginx  for changes to take effect 

sudo systemctl restart nginx

## Key Takeaways
Understanding AWS Services: Gained a deeper understanding of how Ec2, SSL Certificate, and Route 53 work together.

Security: Learned the importance of HTTPS and how to implement it using CertBot.

New tools: Learned how to use external Host domain platform in my case I used http://hostafrica.ke and CertBot

## Resources
- AWS Documentation:

EC2 Static website: 
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-ec2-instance.html

https://yourtechie.hashnode.dev/deploying-a-static-website-to-aws-ec2-with-nginx

## Live Website

personal Domain Link: 
www.nginx.muadmaalim.buzz  or
www.muadmaalim.buzz

