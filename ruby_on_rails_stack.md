# Installfest Step 3: Ruby on Rails Stack (Ruby, Rails, PostgreSQL)

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

![image](./install_rvm.png)


####Install Ruby on Rails 4

After you have installed ruby, we will install a version of Ruby on Rails 4 for the class.

```
gem install rails
```

If this causes errors on your machine, try running `sudo gem install rails` instead.


### PostgreSQL  

#### Postgres.app

1. Download [Postgres.app](http://postgresapp.com/).

2. Follow Postgress.app's install instructions (move Postgres into your Applications folder).
    
3. Follow Postgres.app's [instructions to install command line tools](http://postgresapp.com/documentation/cli-tools.html): 
  * add Postgres.app to your `$PATH`

      ```bash
        echo 'PATH=$PATH:/Applications/Postgres.app/Contents/Versions/9.4/bin' >> ~/.bash_profile
      ```
  * source your `~/.bash_profile`

      ```bash
      source ~/.bash_profile
      ```
  * check that your install worked
    
      ```bash
      which psql
      ```



#### Alternate install with homebrew

Do not follow these instructions unless you have already tried the Postgres.app instructions and spoken to a member of the teaching team.  

<a href="http://exponential.io/blog/2015/02/21/install-postgresql-on-mac-os-x-via-brew/" target="_blank">Instructions for installing postgreSQL with homebrew.</a>


