# CPS493_Web_Server_Programming_Project
## Below all steps I've been following to create this project.

**STEP 1**

        Run int the root folder the "npm init" command, to setup the package.json file and be able to later manage all dependencies. 

**STEP 2**
        
        Created a "client" and "server" folders in the root 

**STEP 3**

        Add the following dependencies to the "package.json"

        "dependencies": {
        "express": "^4.18.2"
        },

        "devDependencies": {
        "nodemon": "^2.0.20"
        }

        -Express: Is a NODE.js web application framework that provides broad features for building web and mobile applications. It is used to build a single page, multipage, and hybrid web application

        -Nodemon: This dependencie will be watching your folder, and when there's a change it restarts the server to see changes. Valid use only for Development purposes, NOT for production. 

        IMPORTANT REMINDER: DONT'T use EJS, DON'T use Express for server side rendering or template.

**STEP 4**

        Run the command "npm i" to install all dependencies.
        Make sure you are in the correct folder!!!! In this case, is the "root"


**STEP 5**

        Add "index.js" in the server folder. With the following code:
        
        const http = require('http');

        const hostname = '127.0.0.1';             
        const port = process.env.PORT || 3000;

        const server = http.createServer((req, res) => {

        res.statusCode = 200;
        res.setHeader('Content-Type', 'text/plain');
        res.end('Enter any text here to display on browser');
        });

        server.listen(port, () => {

        console.log(`Server running at http://${hostname}:${port}/`);
        });



**STEP 6**

        In the "root" run the command "npm init vue@latest"
        This will create the "client" folder and all files and folders. (boilerplate)

        REMINDER
        Package.json       || 
        Package-lock.json  || Keeps track of the version packaging and dependencies version, always keep on GIT.


**STEP 7**

        Running "npm run build"
        Creates the app for production 

**STEP 8**
        Check folder structure, making sure I have the following:
                -assets
                -components     (Here store each individual component that made the page)
                -model          (Logic happens here, for example the session valindation, user info )
                -router         (Links to other pages components)
                -views          
        Delete all VUE default (Hellow World) files, as these are not neeed.