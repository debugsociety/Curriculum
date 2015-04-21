# Think like a computer

## 
Machine name
Label

## How To Ask For Help

When asking for support, or while providing feedback in the form of bugs or
feature requestes, please include the following relevant information:

 - Detailed steps on how to reproduce the problem, including a script that
   reproduces your problem, if possible. 
 - The exact PHP version used. You can find this by running `php -v` on the
   command line, or by checking the output of `phpinfo();` in a script
   requested through a web server.
 - The exact version of the MongoDB driver for PHP. You can find this by
   running `php --ri mongo | grep Version` on the command line, or by running
   a script containing `<?php echo phpversion("mongo"); ?>`.
 - The operating system and version (e.g. Windows 7, OSX 10.8, ...).
 - How you installed the driver, either via your distribution's package
   management, with "brew", with an \*AMP installation package, or through a
   manual source compile and install.
 - With connection and replica set selection issues, please also provide a
   full debug log. See further down on how to make one.

