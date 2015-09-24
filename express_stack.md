#Installfest Step 2: Express Stack (Node.js and MongoDB)

Most of the coding work we do in weeks 3 to 5 will be driven by the back end web development framework <a href="http://expressjs.com/" target="_blank">Express</a>. We'll install express as we go, on a project-by-project basis. For now, we'll install other tools we'll use along with Express.

**Plan overview:**

1. Install Node.js, a platform for back end web development with the JavaScript programming language. 
2. Install JSHint and its Sublime Text packages to get realtime JavaScript syntax hints.
3. Install MongoDB, a database. 

## Node.js

1. Install Node.js with homebrew by running the following command in the Terminal.

  ```
  brew install node
  ```


1. Run the Terminal command `which node` to check that Node.js was installed. The Terminal command `node` changes your Terminal into a Javascript REPL ("Read Evaluate Print Loop"), like the right hand side of repl.it.  Type `control+C` twice to quite out of the REPL and return to the normal Terminal commands.  

1. Run the Terminal command `which npm` to check that npm is installed. The Node Package Manager, used through various `npm` commands, is a lot like Homebrew, except we'll use it for Node.js-specific tools instead of for general Mac tools. NPM packages are often called "node modules."

### Nodemon

Nodemon (short for "node monitor") will make our node.js workflow more efficient. 

Install nodemon globally with the following command:
  
  ```
  sudo npm install -g nodemon
  ```

### JSHint

It's time to install another Sublime Text package!

1. Select `Package Control: Install Package` to bring up the list of available packages.  Select `SublimeLinter` from the list, and Package Control will install it for you.

1. Repeat the step above to install the packages "SublimeLinter-jshint".

1. Follow the <a href="https://github.com/SublimeLinter/SublimeLinter-jshint" target="_blank">SublimeLinter-jshint install instructions</a> to set up jshint on your laptop. You've just installed Node.js and npm, so you won't need to repeat that step.


## MongoDB

MonogDB is a popular noSQL database.  We'll use it to store data with our Node.js stack. 

1. Run brew update to update our brew packages.

  ```bash
  $ brew update
  ```
1. Run `brew install` for **MongoDB**

  ```bash
  $ brew install mongodb
  ```

1. Then we'll need a directory for **MongoDB** to save data.

  ```bash
  $ sudo mkdir -p /data/db
  ```

1. Finally we'll want to make sure we have permission to read and write to this directory.

  ```bash
  $ sudo chown -R $USER /data/db
  ```

1. Run the command `which mongod` to test whether the install worked.  
