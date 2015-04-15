# Git development
Git takes 'snapshots' of the state of files when changes are made. That allows a user to go back to previous versions of files very easily.

### Cloning the Curriculum Repo
Steps to cloning the Curriculum Repo
1. Fork the debugsociety/Curriculum repo on GitHub
2. Copy the HTTPS clone URL from the forked Curriculum repo
3. In the terminal, run the command below:
"git clone 'URL copied from step 2'"

### Create new branch to work on homework file
To work on the files in the Curriculum repo, we create a new branch first.
You can create a new branch with the command below:
"git checkout -b 'name of branch'"

The name of the branch should relate to the changes we are going to make.
If we know we are going to make CSS changes to the jobs offered page for 
example, we might name the branch 'styling-jobs'.

### Push our changes to our repos
We've made some changes, but they are only on our computers. To add them to
our forked GitHub Curriculum repo, we need to commit those changes, and push
them to the repo.
1. Commit the changes you made using the command below:
"git commit -m 'Insert meaningful message describing your change'"
Note: if you added a new file that you would like to include as part of your 
changes, you'll need to run git add first.
2. To push the changes to our repo, we will make use of the git push command.

Run the command "git remote -v" first to see the names of your remote connections. 
If you cloned the Curriculum Repo after forking as mentioned above, you should see 
something like the following:
origin https://github.com/username/Curriculum.git (fetch)
origin https://github.com/username/Curriculum.git (push)

Next, run the command below:
"git push origin 'name of your branch'"
Enter your username and password for GitHub
Note: your password won't display as you type it - this is a security feature :)