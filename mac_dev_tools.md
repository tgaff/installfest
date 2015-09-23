#Installfest Step 1: General Mac Development Tools


**Plan of Attack:**

1. Upgrade operating system to Maverick or Yosemite.   
1. Install Xcode and Command Line Tools - the most basic built-in coding tools for Mac.  
2. Install Homebrew - a package manager for Mac.  (Package managers are programs that help you install external tools and keep them up to date.)
3. Configure git - a version control system. (Version control systems are programs that help you keep track of changes in your code.)
4. Install and configure Sublime Text - a text editor specialized for writing code.
5. Install the Chrome web browser.

If you do not yet have an account for the Mac App Store, follow the instructions on Apple Support to <a href="https://support.apple.com/kb/PH11499?locale=en_US" target="_blank">create a Mac App Store account</a>.

## Operating System and Command Line Tools

Before class starts, we suggest you upgrade your operating system to OS X Maverick or Yosemite. We do not recommend that you use El Capitan *yet* because some of the tools we use have not been updated for El Capitan.  **Do not upgrade your operating system after WDI starts.** 

To check what version of OS X you are running:  
1. Click the apple icon in the top left of your screen.  
2. Select "About This Mac" from the dropdown menu.   
3. Read the version information from the window that pops up.   

If you are not using Maverick or Yosemite, detailed instructions for upgrading your operating system are available through Apple support: <a href="https://www.apple.com/support/osx/upgrade/" target="_blank">How to upgrade to OS X Yosemite</a>.

### Install Command Line Tools from the Terminal

1. Open the Terminal application.
2. In your Terminal, type `xcode-select --install`, and a new window and installer will appear. 
3. Follow the instructions in the installer. 


### Install Command Line Tools through Xcode (Older Versions of OS X)

If you must run a version of OS X before Maverick, you will need to install Command Line tools that come from Xcode.

1. Open the Mac App Store and install Xcode.
1. Open Xcode.
1. Inside the Xcode menu, choose Preferences > Downloads > Install The Command Line Tools.
1. Follow the instructions in the installer.

## Homebrew

<a href="http://brew.sh/" target="_blank">Homebrew</a> is a *package manager* for OS X.  We'll use to quickly download and install other tools we use, or to update already installed tools. 

1. Open up the application Terminal and run the command below to install Homebrew. Wait while homebrew is downloaded and installed.

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

<!-- @TODO - image 
![image](./install_brew.png) -->

1. Run `brew doctor` in your Terminal to check that the install was successful. If there were issues, `brew doctor` will list suggestions for how to fix the issue.  Follow these suggestions one by one. If you are unsure what to do, ask!

1. You may need to edit your ~/.bashrc to have include the path to homebrew, if `brew doctor` returns warnings.

	```
	bash echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.bash_profile
	```


## Git

You should already have git installed and have an account on GitHub from Fundamentals. If not, sign up for an account on <a href="http://www.github.com" target="_blank">http://www.github.com</a>. We will be using github.com to track code and for collaboration. 

### Confirm Install

1. To check whether git is installed on your system, run the Terminal command `which git`. The output should be a directory path like `/usr/bin/git`; this is where git is installed on your machine.


1. If you do not have git installed, run the following command in your Terminal:

	```
	brew install git
	```

### Configure Git

Configuring your git settings to help GitHub track your contributions and to make it easier and smoother to commit. 

1. Use the following three `git config` commands to configure your git user information. We use the `global` option to make the configuration apply to all repos.
  
	```
	git config --global user.name "YOUR-USERNAME"
	git config --global user.email YOUR-EMAIL-ADDRESS
	git config --global credential.helper cache
	```

1. Generate a SSH key for GitHub. This will allow you to use GitHub from your Terminal without entering your login information every time you push.

     [Generating SSH Keys (via GitHub.com)](https://help.github.com/articles/generating-ssh-keys)

## Sublime Text

1. Use the following link to <a href="http://c758482.r82.cf2.rackcdn.com/Sublime%20Text%20Build%203083.dmg">download Sublime Text 3</a>. 

1. Open the file.

1. Follow the installation instructions (drag Sublime Text 3 to your Applications folder).

1. Open the Sublime Text 3 application. 

### Add Package Control and Packages

Sublime Text has its own very popular package manager called Package Control. We'll use it to add extra features to Sublime Text, including a web development package called Emmet and a JavaScript syntax helper called a "linter".

1. Follow <a href="" target="_blank">Package Control's  "simple installation" instructions</a> to add Package manager to your Sublime Text. When you paste the large block of text, make sure you:
   -  use the Sublime Text 3 version, and   
   -  enter the text into the bottom rectangle of the Sublime Text console.

1. We access Package Control through the Sublime Text command palette. Open the palette by pressing `cmd+shift+p` from within Sublime Text. Type `Package Control`  in the command palette to see the list of things Package Control can do.

1. Let's install our first package, Emmet.  Select `Package Control: Install Package` to bring up the list of available packages. 

1. Select `Emmet` from the list, and Package Control will install it for you!  (Start typing "Emmet" in the search bar to narrow down the list.)
