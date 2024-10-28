# MERN WEB STACK - 101
### How does MERN stack work?
![MERN Stack](/MERN_stack_GbyG)
#### [Reference Geeks for Geeks](https://www.geeksforgeeks.org/mern-stack/)

## STEP 0 - Prerequisites
Virtual Server on AWS with Ubuntu Server OS.
![AWS Ubuntu Server](/PROJECT3-MERN/images/AWS_ubuntuOS.png)

## STEP 1 - Backend Configuration

Update Ubuntu OS and adding Node.js repo:

    sudo apt update
    sudo apt upgrade
    curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
    
### Installing Node.js

    sudo apt-get install -y nodejs
    node -v
    npm -v

### Application Code Setup To Do App

Create a **Todo** directory, the run the command:

    npm init

![NPM init](/PROJECT3-MERN/images/todo_npm_init)

### Installing ExpressJS

    npm install express

Create a *index.js* file and install de **dotenv** module:

    touch index.js
    npm install dotenv

![Index js](/PROJECT3-MERN/images/indexjs_creation)

![node index js](/PROJECT3-MERN/images/node_indexjs)

Granted the proper rules to connect to the EC2 server:
![AWS ACL](/PROJECT3-MERN/images/aws_acl_5000)

Check the installation:

![Express Installation](/PROJECT3-MERN/images/express_setup)


### Models

    npm install mongoose
    mkdir models && cd models && touch todo.js

![Mongoose ](/PROJECT3-MERN/images/moongoose)
    
### Creating endpoints for the Todo app:

    mkdir routes
    cd routes
    touch api.js

![API setup](/PROJECT3-MERN/images/api.js)

### MongoDB Database

DBaaS Provisioning of MongoDB Database:
![DBaaS](/PROJECT3-MERN/images/mongodb)

Environment variables to store information is considered a best practice to store secret data.

Updating de *index.js* file:
![indexjs update](/PROJECT3-MERN/images/indexjs_update)

### Testing the backend:
![API GET](/PROJECT3-MERN/images/GET)

![API POST](/PROJECT3-MERN/images/POST)

![DELETE](/PROJECT3-MERN/images/DELETE)

## STEP 2 - Frontend creation

    npx create-react-app client
    npm install concurrently --save-dev
    npm install nodemon --save-dev
![package update](/PROJECT3-MERN/images/packagejson)

    cd client
    nano package.json

Add the key value:
"proxy":"http://localhost:5000"

    npm run dev
![NPM RUN](/PROJECT3-MERN/images/npm_run_dev)

### Creating React Components:

    cd client/src
    mkdir components
    cd components
    touch Input.js ListTodo.js Todo.js

You need to add the code in these three files.

Install axios in **client** folder:

    npm install axios
Then you need to modify the components by adding the necesary code.

For this particular app, the code added produce the following output:

![To Do APP](/PROJECT3-MERN/images/ToDo_app_JE)


    



