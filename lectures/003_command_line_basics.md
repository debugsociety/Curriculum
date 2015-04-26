# Command line basics
If you are new to programming, you likely spend most of your computer-time using a GUI (pronounced gooey). A GUI is a user interface designed to simplify the usage of applications. Unfortunately, a GUI just cannot match the speed and utility of the command line. Once you are comfortable working in the command line, you will be empowered.

## Why complicate things?
*Moving files of type .pdf from the 'Downloads' folder into a folder named Desktop/PDF*
Using the GUI:
- Right click the desktop
- Click 'create new folder'
- Type 'PDF'
- Click elsewhere
- Double click (open) the downloads folder
- Drag and drop each PDF file from downloads to Desktop/PDF
-- If there are a lot of PDF files - good luck!
Time taken: depending on how many files you have in ~/Downloads, likely over 5 minutes.

Using the Command line:
- mkdir ~/Desktop/PDF
- mv ~/Downloads/*.pdf ~/Desktop/PDF
Time taken: 5 seconds.

This is only one example; there are countless others. Once you learn how to use it, the command line will save you plenty of time; even outside of work.

## Basic commands
### ls
- ls => 'list'
- Lists files and folders in the current directory

### cd [relative path to folder]
- 'cd' = >'Change Directory'
- Used for navigating to other folders
- Can use an absolute (entire) path: cd /Users/ashraf/Desktop/debugsociety/subfolder-name
-- Absolute paths begin with a /
- Can use a relative path:
-- cd /Users/ashraf/Desktop
--- Used an absolute path to get to the Desktop folder
-- cd debugsociety
--- Because the debugsociety folder is within my current folder, I can use a relative path.
-- cd subfolder-name
--- Because subfolder-name is in my current folder, I can use a relative path.

### cp [original-file] [destination]
- 'cp' => Copy Paste
- Copies the file [original-file]
- Pastes the file to [destination]
- Example: cp template.html file2.html
-- Copied the file named 'template.html' to a new file named 'file2.html'

### mv [file] [new-location]
- 'mv' => Move
- 'Moves' the file [file] to [new-location]
- Example: mv file2_test.html file2.html
-- Moved the file from file2_test.html to file2.html. In this example, the file was renamed.
- Example 2: mv file2.html files/file2.html
-- Moved file2.html into the relative folder 'files'

### grep '[word]' [file]
- 'grep' => Global regular expression
- To 'grep' for something is to search for it
- Search for [word] in [file]
- 'grepping' is case-sensitive
- *The -r flag makes grep search recursively, rather than only in the current folder.*
- For example:
-- grep -r 'Command lin' ~/Desktop/debugacademy/assignments
-- Will return all files inside the 'assignments' folder which have the word 'Command lin'.

## Short cuts
These shortcuts can be used most anywhere a filename could be used.

### * (asterisks)
- Asterisks means 'anything'.
- In many commands, can be used as part of a filename to expand the command. For example:
- Can be used to select all files in a folder
-- mv files/* files/ashraf/
- Can be used to move files based on a partial filename
-- mv files/*.pdf files/ashraf/
--- This moved everything in the 'files' folder whose name ends in '.pdf'.
-- mv files/a* files/ashraf/
--- This moved everything in the 'files' folder whose name starts with 'a'.
-- mv files/*tmp* files/trash
--- This moved everything in the 'files' folder whose name *contains* 'tmp'.

### ../
- Used to denote 'up one level'
- To change to the directory 'up one level': cd ../
- Can be combined to go up multiple levels:
-- cd ../../
-- That takes you up two levels

### ./
- Used to denote 'current directory'
- Example: mv files/file1.html ./
-- We moved a file from the 'files' folder into the folder we are currently in.
