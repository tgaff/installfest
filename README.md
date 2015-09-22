```md
Based on https://github.com/wdi-sf-july/installfest

## To Do

* test as many instructions as possible on clean computer
* split into multiple readmes so it's not crazy long / hard to read?
* check that Maverick Xcode/Command Line Tools instructions also apply for Yosemite
* completely replace Maverick suggestion with 'upgrade to yosemite'
* completely remove ubuntu and windows instructions?
* copy over images from wdi-sf-july if wanted

## Done

* commented out ubuntu and windows instructions sections
* included instructions for PostgreSQL
* included instructions for Node.js
* included instructions for MongoDB
* added a few notes on what things are / why installing
```

![GA_Logo](https://raw.github.com/generalassembly/ga-ruby-on-rails-for-devs/master/images/ga.png)

#WDI Installfest 

We are going to install most of the tools we'll use in this course onto your computer. We'll install a set of basic tools for programming on OS X, a set of tools specific to our Node.js development stack, and a set for our Ruby on Rails stack.

*In this context, "stack" just refers to a group of technologies used together to create a website.*

If you are unsure or run into problems during installation, don't worry; we will finish up any of the loose ends on Installfest.
	
## General Mac Development Tools


Basic Plan:

1. Upgrade operating system to Maverick or Yosemite.   
1. Install Xcode and/or Command Line Tools - the most basic built-in coding tools for Mac.  
2. Install Homebrew - a package manager for Mac.  *Package managers are programs that help you install external tools and keep them up to date.*    
3. Install git - a version control system. *Version control systems are programs that help you keep track of changes in your code.*    

If you do not yet have an account for the Mac App Store, follow the instructions on Apple Support to <a href="https://support.apple.com/kb/PH11499?locale=en_US" target="_blank">create a Mac App Store account</a>.

### Operating System Version

Before this class, we suggest you upgrade your operating system to OS X Maverick or Yosemite. If you are running one of these most recent versions, you don't have to manually install Xcode in order to get command line tools.  We do not recommend that you use El Capitan *yet* because some of the tools we use have not been updated for El Capitan.

To check what version of OS X you are running:  
1. Click the apple icon in the top left of your screen.  
2. Select "About This Mac" from the dropdown menu.   
3. Read the version information from the window that pops up.   

Detailed instructions for upgrading your operating system are available through Apple support: <a href="https://www.apple.com/support/osx/upgrade/" target="_blank">How to upgrade to OS X Yosemite</a>.

### Install Command Line Tools from Terminal (Maverick/Yosemite)

1. Open the Terminal application.
2. In your Terminal type `xcode-select --install`, and a new window and installer will appear. 
3. Follow the instructions in the installer. 


### Install Command Line Tools through Xcode (Other Versions of OS X)

If you are running a version of OS X before Maverick, you will need to install Command Line tools that come from Xcode.

1. Open the Mac App Store and install Xcode.
1. Open Xcode.
1. Inside the Xcode menu, choose Preferences > Downloads > Install The Command Line Tools.

###Install Homebrew

####Homebrew
[http://brew.sh/](http://brew.sh/)

Open up the application Terminal and run the command below to install Homebrew.

```
ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
```

<!--![image](./install_brew.png)-->

####Brew Doctor

Run `brew doctor` in your Terminal to check that the install was successful. It will give you tips on what you can do to correct any issues. Follow these suggestions to try to resolve any issues.  If you have any questions or unsure what to do, bring your questions to Installfest.


You may need to edit your ~/.bashrc to have include the path to homebrew, if `brew doctor` returns warnings.

```
bash echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.bash_profile
```


### Install and Configure Git

You should already have git installed and have an account on GitHub from Fundamentals. If not, sign up for an account on <a href="http://www.github.com" target="_blank">http://www.github.com</a>. We will be using github.com for for keeping track of code and for collaboration. 

To check whether git is installed on your system, run the Terminal command `which git`. The output should be a directory path; this is where git is installed on your machine.


####Install git with homebrew

If you do not have git installed, run the following command in your Terminal:

```
brew install git
```


####Update git config information

Configuring your git settings to help GitHub track your contributions and to make it easier and smoother to commit. 

1. Use the following three commands to set up your configure your git user information. Normally, you would have to redo the configuration every time you make a repo. We use the `global` option to make the configuration apply to all repos.
  
  ```
  git config --global user.name "YOUR-USERNAME"
  git config --global user.email YOUR-EMAIL-ADDRESS
  git config --global credential.helper cache
  ```

1. Generate a SSH key for github. Follow the instructions below to use GitHub from your Terminal without having to input your login credentials every time.

     [Generating SSH Keys (via Github.com)](https://help.github.com/articles/generating-ssh-keys)

## Node.js and Express Tools

Basic Plan:

1. Install Node.js, a platform for back end web development with the JavaScript programming language. 
2. Install Express.js, a back end web development framework. 
3. Install MongoDB, a database. 

### Node.js

Install Node.js with homebrew by running the following command in the Terminal.

```
brew install node
```

Run the Terminal command `which node` to check that Node.js was installed. 

Node.js comes with some cool tools, including `node` and `npm`.  The Terminal command `node` changes your Terminal into a Javascript REPL ("Read Evaluate Print Loop"), like from repl.it.  Type `control+C` twice to quite out of the REPL and return to the normal Terminal commands.  The Node Package Manager, used through various `npm` commands, is a lot like Homebrew, except we'll use it for Node.js-specific tools instead of for general Mac tools. NPM packages are often called "node modules."

## MongoDB

## Ruby on Rails Tools

Our Ruby on Rails stack will reuse the front end tools we start the class with. It will introduce Ruby on Rails as our back end framework and PostgreSQL as our database. 

###Verify Previously Installed Versions

If you have already experimented with ruby or Ruby on Rails before, verify your versions are correct for this upcoming class.

1. In your Terminal, run `ruby --version`.  The output will include the version number of ruby you have installed. **Verify you are running 2.0+ of ruby**.

1. In your Terminal, run `rails --version`. **Verify you are running version 4 of Ruby on Rails**.


If you are using an earlier version of ruby or Ruby on Rails, continue with the instructions to get your environment set up. Run these version commands in the Terminal again after you're done to ensure everything is working properly.


### Install RVM and Rails

####RVM and Ruby

RVM is a Ruby Version Manager. It lets you easily switch between versions of the ruby programming language.

####Install RVM with Ruby

[http://www.rvm.io](http://www.rvm.io) for full instructions


Run the following command to install the latest version of Ruby, as well as RVM.

```
\curl -L https://get.rvm.io | bash -s stable --ruby
```

<!--![image](./install_rvm.png)-->


####Install Ruby on Rails 4

After you have installed ruby, we will install a version of Ruby on Rails 4 for the class.

```
gem install rails
```

If this causes errors on your machine, try running `sudo gem install rails` instead.


### PostgreSQL  

To install the PostgreSQL database, run the following command in your Terminal.

```
brew install postgresql
```

Run `which psql` in the Terminal to check that PostgreSQL was installed.


<!--#Ubuntu Instructions -->



<!--##apt-get-->

<!--###Install apt-get-->
<!--```-->
<!--sudo apt-get install curl-->
<!--```-->

<!--##rvm & ruby-->

<!--###Install RVM-->
<!--```-->
<!--\curl -L https://get.rvm.io | bash -s stable --ruby-->
<!--```-->


<!--##rails-->

<!--###Install Rails 4-->
<!--```-->
<!--gem install rails-->
<!--```-->


<!--##git-->

<!--###Install git-->
<!--```-->
<!--sudo apt-get install git-core-->
<!--```-->

<!--###Update git config information-->

<!--```-->
<!--git config --global user.name "YOUR-USERNAME"-->
<!--git config --global user.email YOUR-EMAIL-ADDRESS-->
<!--git config --global credential.helper cache-->
<!--```-->


<!--===-->

<!--#Windows Users-->


<!--**Ruby Installer:**-->

<!--The install on Windows is actually very with the bundle from [rubyinstaller.org](http://www.rubyinstaller.org)-->

<!--Just be sure to grab the 2.0.0 version, as that will be the version we will be using in class. This will set up your environment and you can start running ruby files right away. -->

<!--To install rails, run the following command `gem install ruby`-->


<!--**Extra command line tools: **-->

<!--We will be using the command line a lot here. On Windows I also like to install gow. Gow is a bunch of unix command line tools ported to Windows. It will make it easy to follow in class with the same commands as your Mac buddies. -->

<!--[https://github.com/bmatzelle/gow/wiki](https://github.com/bmatzelle/gow/wiki)-->
