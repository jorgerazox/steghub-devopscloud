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


## Step 5: Install MySQL

1. Install MySQL using the following commands:

```bash
sudo apt install mysql-server
```

2. Log in  to the MySql Console:

```bash
sudo mysql
```

![MYSQL CONSOLE](/PROJECT2-LEMP/images/MySqlConsole.png)

3.  Secure the MySQL installation:


```bash
sudo mysql_secure_installation
```

Follow the prompts to set a root password, remove anonymous users, disable remote root login, and remove the test database.

4. To log in to MySQL as the root user, use:

```bash

sudo mysql -p

```

## Step 6: Install PHP
PHP - NGINX ARCHITECTURE
![PHP NGINX ARCHITECTURE](/PROJECT2-LEMP/images/PHPNGINXARCH.png)

1. Install PHP and the necessary PHP modules:
```bash

sudo apt install php-fpm php-mysql

```

2. Configuring Nginx to Use PHP Processor:

2.1 Create a directory

```bash

sudo mkdir /var/www/projectLEMP

```
2.2 Assign ownership to the directory:

```bash
sudo chown -R $USER:$USER /var/www/projectLEMP

```
2.3 Create a Nginx configuration file:

```bash

$ sudo nano /etc/nginx/sites-available/projectLEMP

```

```vscode
#/etc/nginx/sites-available/projectLEMP

server {
    listen 80;
    server_name projectLEMP www.projectLEMP;
    root /var/www/projectLEMP;

    index index.html index.htm index.php;

    location / {
        try_files $uri $uri/ =404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php8.3-fpm.sock;
     }

    location ~ /\.ht {
        deny all;
    }

}
```

2.4 Enable the site, check syntax error and disable default site:

```bash

sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/
sudo nginx -t 
sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/

```

2.5 Reload Nginx:

```bash

sudo systemctl reload nginx

```

2.6 Test the new website

```vbnet
http://<ec2-public-ip>:80

```

![NGINX SITE](/PROJECT2-LEMP/images/NewSiteNginx.png)

## Step 7: Testing PHP with Nginx
1. Set up info.php:

```bash

nano /var/www/projectLEMP/info.php

```
![PHP Test](/PROJECT2-LEMP/images/PHPNginxTEST.png)

2. Remove the info.php:
```bash

sudo rm /var/www/projectLEMP/info.php

```

## Step 7: Retrieving data from MySQL database with PHP

A TO DO list in PHP with data retrieved form MYSQL.

![TO DO List example](/PROJECT2-LEMP/images/PHPMYSQLQuery.png)

---
