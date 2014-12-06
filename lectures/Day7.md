# Day 7: Debugging a conflict

## After turning on your classmates' features, you may have seen an error
Each person in the class created a content type with various fields. They then exported them to features, pushed them to git, and shared them with the class. Everyone turned on all of their classmates' features and - boom - your site may have crashed. What now?

## There is no magic in programming
Let's think about this - what just happened?
1. Everyone created a content type
- no problems so far
2. Everyone added fields to their content types
- still looking good
3. Everyone exported their content types and fields
- no errors
4. Everyone enabled their classmates' features. AKA they turned on  all of their classmates' content types and fields on
- :( The site crashed

Okay - all looked good until step 4. My classmates' content types broke my site.

## Analyzing the problem
Turning my classmates' content types on broke the site. Let's turn them off (using drush) and see if that fixes it.
Clear the cache and... site's back!




Run a rough 'health diagnosis' on homework assignments
Implement the 'HTML Outliner' tool from the tools repo on your homework assignment.
Open your homework assignment. Click 'Debug' - do the outlines of your HTML look appropriate?

### As a class, improve the roughest looking homework assignment
1. Cut a new branch
2. Turn 'Debugging' on (Debugger tool)
3. Run through the file - talk through issues, correct them on the spot
4. Run 'Debug' after correcting the file together
5. Rejoice

## Download and Install Drupal 7
Note: This assumes your local environment was set up with our class
1. Open the command line (terminal or Git Bash)
2. cd into our Sites/vdd folder
3. Go to your server ( 192.168.44.44 )
-- If your server is up (page says 'Welcome to VDD!'), continue to step 4
-- Otherwise, run 'vagrant reload' from within your 'vdd' folder
---- When this completes, repeat step 3
4. Go to Drupal.org, download the latest Drupal 7.X stable version
-- https://www.drupal.org/project/drupal 
-- The latest stable 7.x version is highlighted in green
-- Download either the 'zip' or the 'tar.gz' - whatever your computer can unzip
5. Unzip the downloaded file
6. Move the unzipped folder (will be named drupal-7.XX) into Sites/vdd/data
-- The unzipped folder will now be located in vdd/data/drupal-7.XX
7. cd into Sites/vdd
8. SSH into your vagrant box (vagrant ssh)
9. Create a mysql database by running the following commands (only type the parts after '--:')
--: mysql -uroot -proot # this connects to your mysql database via the command line
--: create database myfirstdrupalsite; -- this creates a database named myfirstdrupalsite. don't leave out the semicolon.
--: exit; -- leaves the mysql command line editor
10. In your browser, go to 192.168.44.44/drupal-7.X (replace the 'drupal-7.X' with the name of the folder you downloaded)
11: Run through the installation steps
-- When it asks you to pick between 'Standard' or 'Minimal', choose Standard
-- When it asks for your database username, password, and name, enter the following:
---- Username: root
---- Password: root
---- Database name: myfirstdrupalsite
12: Click 'next' and fill in the required fields until your site begins installing
13: Look around your new Drupal 7 website!
