# Day 1: Orientation, set up

## Download and install the following software

### Windows users


### Mac users


## Set up a local development environment with Vagrant

Create a folder on your desktop called Sites

Download the most recent stable version of the drupal vdd project: https://www.drupal.org/project/vdd
- (download the zip file highlighted in green on that page)
Unzip that file, place the 'vdd' folder in Desktop/Sites/

Stop and do the following 2 tutorials if you're unfamiliar with using command line:
1. http://ryanstutorials.net/linuxtutorial/commandline.php
2. http://ryanstutorials.net/linuxtutorial/navigation.php

Using command prompt (or terminal if a mac user), navigate to Desktop/Sites/vdd 
- In the command prompt, execute the command: vagrant up
- This command will take a while. Go to 192.168.44.44 in your browser to check if it finished successfully. 
  If so, that page will say *Welcome to VDD!*
  If not, and you are very confident that the script has completed, then run vagrant up again.

## Use what you've installed

### Windows users
Open git bash
Go to the Desktop/Sites/vdd folder
Execute the command: vagrant ssh
Execute the command: ls
You should see a folder called sites. Enter that folder
Execute the command: git clone https://github.com/debugsociety/tools.git
You should now have a local copy of tools posted for the class

### Mac users
Open the terminal
Go to the Desktop/Sites/vdd folder
Execute the command: vagrant ssh
Execute the command: ls
You should see a folder called sites. Enter that folder
Execute the command: git clone https://github.com/debugsociety/tools.git
You should now have a local copy of tools posted for the class

## Accounts setup 

Create accounts at the following websites:
github.com
drupal.org
slack.com (you will receive an invite)

