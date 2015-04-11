# Set Up a Drupal Website

## Download Drupal
1. Go to Drupal.org, download the latest Drupal 7.X stable version
-- https://www.drupal.org/project/drupal 
-- The latest stable 7.x version is highlighted in green
-- Download either the 'zip' or the 'tar.gz' - whatever your computer can unzip
2. Unzip the downloaded file

### Install Drupal Using Acquia Dev Desktop
1. Clone the website's repo to your local computer
2. Open Acquia Dev Desktop 2
3. Click on the (+) in the bottom left corner of the window and choose "Import local Drupal site"
4. For (local codebase folder) select the local repo
5. Fill in (local site name) with an appropriate name for your website
6. Leave it set to "create new database"
7. After clicking "ok," click on your local site link 
8. Start going through the installation process; leave "standard" and "english" selected, clicking save and continue each time.
9. Fill in all of the required fields,click save and continue.
10. Enjoy your new website!

### Install Drupal Using Vagrant
Note: This assumes your local environment was set up with our class
1. Open the command line (terminal or Git Bash)
2. cd into our Sites/vdd folder
3. Go to your server ( 192.168.44.44 )
-- If your server is up (page says 'Welcome to VDD!'), continue to step 4
-- Otherwise, run 'vagrant reload' from within your 'vdd' folder
---- When this completes, repeat step 3
4. Move the unzipped folder (will be named drupal-7.XX) into Sites/vdd/data
-- The unzipped folder will now be located in vdd/data/drupal-7.XX
5. cd into Sites/vdd
6. SSH into your vagrant box (vagrant ssh)
7. Create a mysql database by running the following commands (only type the parts after '--:')
--: mysql -uroot -proot # this connects to your mysql database via the command line
--: create database myfirstdrupalsite; -- this creates a database named myfirstdrupalsite. don't leave out the semicolon.
--: exit; -- leaves the mysql command line editor
8. In your browser, go to 192.168.44.44/drupal-7.X (replace the 'drupal-7.X' with the name of the folder you downloaded)
9: Run through the installation steps
-- When it asks you to pick between 'Standard' or 'Minimal', choose Standard
-- When it asks for your database username, password, and name, enter the following:
---- Username: root
---- Password: root
---- Database name: myfirstdrupalsite
10: Click 'next' and fill in the required fields until your site begins installing
11: Look around your new Drupal 7 website!
