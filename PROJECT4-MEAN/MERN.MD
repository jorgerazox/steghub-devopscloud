# MEAN Stack Deployment

# Simple Book Register

## STEP 0 - EC2 Deployment

EC2 Instance deployment in AWS account: 

![MERN EC2](/PROJECT4-MEAN/images/EC2VM.png)

## STEP 1 - Install Node JS

Apply Ubuntu updates:

    sudo apt update
    sudo apt upgrade
    
 Adding certificates:
 
    sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates curl -sL
    https://deb.nodesource.com/setup_18.x | sudo -E bash -	

Installing NodeJS

    sudo apt install -y nodejs

![NODE JS](/PROJECT4-MEAN/images/NodeJSVersion.png)

## STEP 2 MongoDB Install

For MongoDB installation, the follow reference was used:
[# How To Install MongoDB on Ubuntu 20.04 by Mark Drake ](https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-20-04)

![MONGO DB](/PROJECT4-MEAN/images/MongoDBInstalled.png)

NPM installation:

    sudo apt install npm

**body-parser** package installation:

    sudo npm install body-parser

**Book Management** directory structure:

![Book Structure](/PROJECT4-MEAN/images/BookManagementeDirectory.png))

To initialize the npm project, run the following command on the **/Books** and use the **server.js** file to add webserver code:

    npm init
    nano server.js

## STEP 3 Express installation

Express & Mongoose installation:

    sudo npm install express mongoose

Create **/app** structure and **routes.js** to server:

![BookAppsDir](/PROJECT4-MEAN/images/BooksAppDir.png)

Create **/models** and **books.js** file:

![ModelBooks](/PROJECT4-MEAN/images/ModelBooks.png)

## STEP 4 Access routes with Angular JS

Create **/public** and **scripts.js** file:

![AngularRoute](/PROJECT4-MEAN/images/AngularRoute.png)

The **index.html** directory is also created in here.

Start the server:

    node server.js

![Running server](/PROJECT4-MEAN/images/RuningServer.png)

**Simple Book Register** running from Internet:

![BookManagement](/PROJECT4-MEAN/images/BookManagement.png)


