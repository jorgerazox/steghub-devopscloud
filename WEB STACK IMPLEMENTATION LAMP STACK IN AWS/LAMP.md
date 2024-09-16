# Generica guide to Set Up a AMP stack (Linux, Apache, MySQL, PHP) on an EC2 Instance (AWS)

## Prerequisites

1. **AWS Account**: AWS account to create an EC2 instance.
2. **EC2 Instance**: Ubuntu Linux 2 EC2 instance with a security group allowing SSH (port 22), HTTP (port 80).
3. **SSH Access**: A private key (`.pem` file) to SSH into your EC2 instance.

---

# Step 1: Launch an EC2 Instance

1. Log in to the [AWS Management Console](https://aws.amazon.com/console/).
2. Navigate to the **EC2 Dashboard**.
3. Click on **Launch Instance**.
4. Choose **Ubuntu Server 24.04 LTS (HVM), SSD Volume Type**.
5. Select an instance type t2.micro (free tier eligibility).
6. Configure security group to allow:
   - SSH (port 22)
   - HTTP (port 80)
7. Review and launch the instance, and download your `.pem` key pair.

---

## Step 2: Connect to Your EC2 Instance via SSH

Use the following command to SSH into your EC2 instance from your terminal:

```bash
ssh -i "your-key.pem" ec2-user@<ec2-public-ip>


## Step 3: Update the EC2 Instance

Update the system's package repository to ensure you are installing the latest versions of software:

```bash
sudo apt update && sudo apt upgrade -y


## Step 4: Install Apache Web Server

1. Install Apache using the following command:

    ```bash
  sudo apt install apache2 -y

    ```

2. Start the Apache service:

    ```bash
    sudo systemctl start httpd
    ```

3. Enable Apache to start on boot:

    ```bash
    sudo systemctl enable httpd
    ```

4. Verify Apache is running by accessing your EC2 instance's public IP address in your browser:

    ```
    http://<ec2-public-ip>
    ```

---

## Step 5: Install MySQL

1. Install MySQL using the following commands:

    ```bash
    sudo apt install mysql-server -y
    ```

2. Start the MySQL service:

    ```bash
    sudo systemctl start mysqld
    ```

3. Enable MySQL to start on boot:

    ```bash
    sudo systemctl enable mysqld
    ```

4. Secure the MySQL installation:

    ```bash
    sudo mysql_secure_installation
    ```

    Follow the prompts to set a root password, remove anonymous users, disable remote root login, and remove the test database.

5. To log in to MySQL as the root user, use:

    ```bash
    mysql -u root -p
    ```

---

## Step 6: Install PHP

1. Install PHP and the necessary PHP modules:

    ```bash
    sudo apt install php libapache2-mod-php php-mysql -y
    ```

2. Restart Apache to load PHP:

    ```bash
    sudo systemctl restart apache2
    ```

---

## Step 7: Test PHP

1. Create a PHP info file to verify PHP is working:

    ```bash
    sudo echo "<?php phpinfo(); ?>" > /var/www/html/info.php
    ```

2. Access the following URL in your browser to view the PHP info page:

    ```
    http://<ec2-public-ip>/info.php
    ```

    You should see a page with details about your PHP installation.

---
