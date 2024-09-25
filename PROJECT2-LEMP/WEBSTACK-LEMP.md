# Guide to Set Up a LEMP Stack on an EC2 Instance (Ubuntu 24)


## Prerequisites

1. **AWS Account**: You need an AWS account to create an EC2 instance.
2. **EC2 Instance**: An Ubuntu 24 EC2 instance with a security group allowing SSH (port 22), HTTP (port 80), and HTTPS (port 443).
3. **SSH Access**: Ensure you have the private key (`.pem` file) to SSH into your EC2 instance.

---

## Step 1: Launch an EC2 Instance

1. Log in to the [AWS Management Console](https://aws.amazon.com/console/).
2. Navigate to the **EC2 Dashboard**.
3. Click on **Launch Instance**.
4. Choose **Ubuntu Server 24.04 LTS (HVM), SSD Volume Type**.
5. Select an instance type (e.g., `t2.micro` for free tier eligibility).
6. Configure security group to allow:
   - SSH (port 22)
   - HTTP (port 80)
   - HTTPS (port 443)
7. Review and launch the instance, and download your `.pem` key pair.

---

## Step 2: Connect to Your EC2 Instance via SSH

Use the following command to SSH into your EC2 instance from your terminal:

```bash

ssh -i "your-key.pem" ubuntu@<ec2-public-ip>

```
![AWS EC2 LEMP](/PROJECT2-LEMP/images/AWS%20EC2%20LEMP.png)

## Step 3: Update the EC2 Instance

Update the system's package repository to ensure you are installing the latest versions of software:

```bash

sudo apt update 
sudo apt install nginx

```

## Step 4: Install Nginx Web Server

1. Install Nginx using the following command:

```bash

sudo apt install nginx

```


2. Check the Nginx service status:

```bash

sudo systemctl status nginx
```
![NGINX STATUS](/PROJECT2-LEMP/images/NgincStatus.png)

3. Enable TCP Port 80:

![NGINX STATUS](/PROJECT2-LEMP/images/TCP80.png)



4. Verify Nginx is running by accessing your EC2 instance's public IP address in your browser:

```vbnet

http://<ec2-public-ip>

```

![NGINX PUBLIC](/PROJECT2-LEMP/images/NginxPublic.png)

or

```bash

curl http://localhost:80

```
![NGINX LOCAL](/PROJECT2-LEMP/images/NginxLocalhost.png)
