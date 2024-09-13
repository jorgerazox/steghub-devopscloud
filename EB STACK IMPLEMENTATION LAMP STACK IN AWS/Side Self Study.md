# Software Development Life Cycle (SDLC)

The Software Development Life Cycle (SDLC) is a structured process used for developing software applications. It outlines the stages involved in the creation of software from its initial concept to deployment and maintenance. The SDLC ensures that the software meets business requirements and is of high quality. 

## Key Phases:

### 1. Planning
Define the project’s scope, objectives, and feasibility. Resources, timelines, and costs are estimated.

### 2. Requirements Analysis
Gather and analyze the specific needs and requirements of the stakeholders. This results in a clear understanding of what the software should do.

### 3. Design
Architects and developers create the technical specifications, system architecture, and design models. This phase involves both high-level and detailed designs.

### 4. Implementation (Coding)
Developers write the actual code for the software based on the design specifications. This is where the product is built.

### 5. Testing
The software is rigorously tested for bugs, performance issues, and security vulnerabilities to ensure it meets the defined requirements and functions properly.

### 6. Deployment
The completed software is deployed to the production environment, making it available for users. It can involve different approaches like phased rollouts or full releases.

### 7. Maintenance
After deployment, the software enters the maintenance phase where bugs are fixed, updates are made, and the software is continuously improved.

---

The SDLC is important for managing the complexities of software projects and ensuring successful delivery. Models like **Waterfall**, **Agile**, and **DevOps** follow different approaches to the SDLC process.

---

# Agile Approach to SDLC

The **Agile** approach to the Software Development Life Cycle (SDLC) is a methodology that emphasizes flexibility, collaboration, and iterative development. It differs from traditional models (like Waterfall) by focusing on continuous feedback, incremental delivery, and adaptive planning.

## Key Principles of Agile in SDLC

1. **Iterative Development**: Agile breaks down the project into smaller, manageable pieces called _iterations_ or _sprints_. Each iteration results in a working product increment that can be reviewed and improved in future cycles.

2. **Customer Collaboration**: In Agile, stakeholders and customers are continuously involved throughout the project. Regular feedback helps ensure that the product meets their evolving requirements.

3. **Adaptive Planning**: Unlike traditional models, Agile is flexible and adapts to changes in requirements, even late in the development process. Plans are adjusted regularly to reflect feedback and changes.

4. **Cross-functional Teams**: Agile promotes collaboration across different team members, including developers, testers, and business analysts. These teams work together to deliver working software at the end of each iteration.

5. **Continuous Improvement**: After each sprint, teams hold a _retrospective_ to assess what went well and what could be improved. This allows for ongoing optimization of the development process.

## Phases of SDLC in Agile

1. **Concept/Initiation**: Identify the project vision and create an initial backlog of requirements. The focus is on understanding the high-level needs.
   
2. **Requirements**: Unlike traditional models where all requirements are gathered upfront, Agile collects and refines requirements continuously throughout the project.

3. **Design**: Design is incremental, evolving with each sprint. The design work is done just in time for the relevant sprint.

4. **Development**: Developers work on a small set of features in each sprint. At the end of the sprint, working software is delivered, which includes coding, unit testing, and integration.

5. **Testing**: Testing happens throughout each sprint. Instead of waiting until the end, testers work with developers to validate each increment during the sprint.

6. **Deployment**: Software increments are deployed frequently, often after every sprint. This could be in the form of a beta release or a full production deployment.

7. **Review/Feedback**: At the end of each sprint, teams present their work in a _sprint review_ or demo, where stakeholders provide feedback.

8. **Retrospective**: Teams hold a retrospective to analyze the sprint's performance and identify areas for improvement in the next cycle.

## Benefits of Agile SDLC

- **Faster Time to Market**: Delivering incremental improvements allows organizations to get working software into the hands of users quickly.
- **Flexibility**: Agile’s adaptive nature allows teams to pivot and make changes based on feedback and new information.
- **Collaboration**: Regular communication with stakeholders and between team members promotes transparency and better outcomes.
- **Continuous Delivery**: Agile teams are able to release new features and updates frequently, ensuring a continuous stream of improvements.

## Common Agile Frameworks

- **Scrum**: A popular framework for managing the Agile SDLC with fixed-length iterations called sprints (usually 2-4 weeks).
- **Kanban**: Focuses on continuous delivery without fixed-length iterations and emphasizes visualizing workflows.
- **Extreme Programming (XP)**: Prioritizes technical excellence and frequent releases, focusing on customer satisfaction.

---

# LAMP Stack

The **LAMP stack** is a popular open-source software stack used for web development. It is an acronym that stands for:

- **L**inux (Operating System)
- **A**pache (Web Server)
- **M**ySQL or MariaDB (Database)
- **P**HP, Perl, or Python (Programming Language)

These four components work together to build dynamic websites and web applications.

## Components of the LAMP Stack

1. **Linux**: 
   - The operating system that provides the foundation for the LAMP stack.
   - Linux is known for its security, stability, and scalability, making it ideal for web hosting environments.

2. **Apache**:
   - A widely-used open-source web server software that handles requests and serves web pages to users.
   - It processes incoming HTTP requests and delivers HTML and other content to the user's browser.

3. **MySQL** or **MariaDB**:
   - A relational database management system (RDBMS) used to store and manage data for dynamic websites.
   - **MySQL** is the most common, but **MariaDB** is a fork of MySQL that is gaining popularity.
   - This database stores user data, application data, and content that is served by the website.

4. **PHP**, **Perl**, or **Python**:
   - Programming languages that are used to build the dynamic part of websites and web applications.
   - **PHP** is the most widely used in the LAMP stack, allowing web servers to execute dynamic content and interact with the database.
   - **Perl** and **Python** are also compatible and sometimes used in place of PHP for specific projects.

## How the LAMP Stack Works

1. **Client Request**: A user requests a webpage through their web browser.
2. **Apache Server**: The request is handled by the Apache web server running on a Linux-based machine.
3. **PHP Processing**: If the request involves dynamic content (e.g., accessing data from a database), PHP processes the request.
4. **Database Query**: PHP interacts with the MySQL or MariaDB database to retrieve or update the necessary data.
5. **Response**: The web server sends the dynamically generated content (HTML, images, etc.) back to the user's browser.

## Benefits of the LAMP Stack

- **Open Source**: All components are open-source, which means no licensing fees and a large community of support.
- **Flexibility**: Each component can be replaced or upgraded individually (e.g., switching from MySQL to MariaDB).
- **Security**: Linux offers a secure environment, and regular updates ensure the stack remains protected.
- **Scalability**: The LAMP stack can handle high-traffic websites and large-scale applications.

## Use Cases

- **Content Management Systems (CMS)**: Platforms like WordPress, Joomla, and Drupal are built on the LAMP stack.
- **eCommerce Websites**: Many online stores, such as those powered by Magento, use LAMP.
- **Web Applications**: LAMP is commonly used for building web apps like social networks, blogs, and more.

## Alternatives to the LAMP Stack

- **LEMP Stack**: Replaces Apache with **Nginx** for better performance in certain scenarios.
- **MEAN Stack**: Uses **MongoDB**, **Express.js**, **Angular**, and **Node.js**—popular for JavaScript-based development.

---

# File Access and Ownership in Linux

Linux systems use file permissions and ownership to control who can read, write, and execute files and directories. Two essential commands for managing permissions and ownership are `chmod` and `chown`.

## `chmod` Command

The `chmod` command changes the permissions of files or directories. There are three types of permissions:

- **r** (read): Allows viewing the contents of a file or directory.
- **w** (write): Allows modifying a file or the contents of a directory.
- **x** (execute): Allows executing a file (if it's a script or binary) or accessing a directory.

### File Permission Structure

Each file or directory has three sets of permissions:

1. **User (Owner)**: The person who owns the file.
2. **Group**: A group of users with similar access needs.
3. **Others**: Everyone else who has access to the system.

### Changing Permissions with `chmod`

Permissions can be changed either numerically or symbolically.

- **Numerical Mode**: Permissions are represented by numbers (r=4, w=2, x=1).
  - Example: `chmod 755 filename`
    - 7 (owner): read (4) + write (2) + execute (1) = 7
    - 5 (group): read (4) + execute (1) = 5
    - 5 (others): read (4) + execute (1) = 5

- **Symbolic Mode**: Uses letters and operators (+, -, =) to set permissions.
  - Example: `chmod u+x filename`
    - Adds execute (`x`) permission to the user (owner).

### Common `chmod` Examples

- `chmod 644 file.txt`: Owner can read/write, others can read.
- `chmod 755 script.sh`: Owner can read/write/execute, others can read/execute.
- `chmod u+rwx,g+rx,o-r file.txt`: Give full permissions to the owner, read/execute to the group, and remove read permission from others.

## `chown` Command

The `chown` command changes the ownership of files or directories. It allows you to change both the owner and group associated with a file.

### Changing Ownership with `chown`

- **Basic Syntax**: `chown [owner]:[group] file`
  - Example: `chown jorge:admin file.txt`
    - This changes the owner to **jorge** and the group to **admin**.

### Common `chown` Examples

- `chown jorge file.txt`: Change only the owner to **jorge**.
- `chown :admin file.txt`: Change only the group to **admin**.
- `chown -R jorge:admin /var/www`: Recursively change ownership of all files in a directory.

## Understanding File Permissions and Ownership

1. **File Permissions**: Controlled by the `chmod` command, which manages the read, write, and execute rights for the user (owner), group, and others.
2. **File Ownership**: Controlled by the `chown` command, which determines who owns the file and what group has access to it.
3. **Execution Permissions**: For scripts or binaries to run, the user must have execute (`x`) permission.

---

# TCP and UDP: Glossary and Commonly Used Ports

## Glossary

- **TCP (Transmission Control Protocol)**: A connection-oriented protocol that ensures data is delivered accurately and in the correct sequence. It establishes a connection before transferring data, making it more reliable but slower due to error-checking and retransmission.
  
- **UDP (User Datagram Protocol)**: A connectionless protocol that sends data without establishing a connection. It's faster than TCP but less reliable, as it doesn't guarantee that packets arrive in order or are even delivered at all. Ideal for time-sensitive applications like video streaming and gaming.

## Commonly Used Ports

| **Port Number** | **Protocol** | **Description**                |
|-----------------|--------------|--------------------------------|
| **20**          | TCP          | FTP (File Transfer Protocol) Data Transfer |
| **21**          | TCP          | FTP Command Control            |
| **22**          | TCP          | SSH (Secure Shell)             |
| **23**          | TCP          | Telnet (Unencrypted Communication) |
| **25**          | TCP          | SMTP (Simple Mail Transfer Protocol) |
| **53**          | TCP/UDP      | DNS (Domain Name System)       |
| **67/68**       | UDP          | DHCP (Dynamic Host Configuration Protocol) |
| **80**          | TCP          | HTTP (Hypertext Transfer Protocol) |
| **110**         | TCP          | POP3 (Post Office Protocol)    |
| **143**         | TCP          | IMAP (Internet Message Access Protocol) |
| **443**         | TCP          | HTTPS (HTTP Secure)            |
| **993**         | TCP          | IMAPS (IMAP over SSL/TLS)      |
| **995**         | TCP          | POP3S (POP3 over SSL/TLS)      |
| **3306**        | TCP          | MySQL Database Service         |
| **3389**        | TCP          | Remote Desktop Protocol (RDP)  |
| **5432**        | TCP          | PostgreSQL Database Service    |
| **5900**        | TCP          | VNC (Virtual Network Computing) |
| **8080**        | TCP          | HTTP Alternate (Commonly Used for Web Servers) |

---

