# Day 1: Orientation and set up

## Download and install the following software

### Windows users
Download & Install VirtualBox
https://www.virtualbox.org/wiki/Downloads
(VirtualBox 4.3.16 for OS X hosts  x86/amd64)

Download & Install Vagrant
(Latest version from https://www.vagrantup.com/downloads.html)

Download & Install git bash
http://msysgit.github.io

### Mac users
Download & Install VirtualBox
https://www.virtualbox.org/wiki/Downloads
(VirtualBox 4.3.16 for OS X hosts  x86/amd64)

Download & Install Vagrant
(Latest version from https://www.vagrantup.com/downloads.html)

Downliand & Install xCode (from the app store)

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

## Download and install the Acquia DEV desktop 2

Acquia Dev Desktop 2 allows you to install, test, and build Drupal sites locally on your Mac or Windows PC and optionally host them on either Acquia Cloud or the Acquia Cloud Free developer sandbox. Easily push or pull to synchronize your local site's code, database, or files with any Acquia Cloud environment. 

### Download link: https://www.acquia.com/downloads 

## Local environment setup 

1. Start Acquia DEV Desktop 2
2. Select "Get started"
3. Select "Start from scratch,I don't have an existing Drupal site"
4. choose to install Drupal v7.2
5. choose where to install drupal ex: Desktop\Drupal Sites\FirstDrupalSite
6. After installation is complete you should see the name of the website on the left "website name.local", click on it to open it.

## Configuring your web site

## Accounts setup 

Create accounts at the following websites:
github.com
drupal.org
slack.com (you will receive an invite)
