# Git development

## Basics of Git
Git is a Version Control System, or 'VCS'. It takes snapshots of the state of files when changes are made. It is extremely beneficial and necessary on any large software project.

### Benefits of your team using Git
- Teammates can work on the same files at the same time
- Teammates cannot overwrite each other's files
- The latest files can be pulled from one place
- You can revert to an older version of the files at any time
- You can easily tell if anyone made changes to any of your files
- You can easily tell who made what changes to each file

### Git Terminology
- *Git Repository* ('Repo'): A folder which uses Git version control. Unless explicitly excluded, changes to files in this folder are tracked by Git, and history can easily be recorded.
- *Branch*: A 'version' of a repository. Branches exist in parallel. Unless explicitly merged, work on each branch remains unaffected by work on other branches.
- *Tag*: A 'snapshot' of a repository at a certain point in time.
- *Checkout*: Checkout is a command used for switching to a different branch (version) of the same repository.
- *Fork*: A personal copy of a repository. If you see a repository you want to work on, you can fork (copy) it, and make all the changes you want to your forked copy.
- *Merge*: To combine work from another source (e.g. version, branch, or commit) into your current branch.
-- For example, assume I edited 'homepage.html' on my branch1, and subpage.html on my branch2. I now want to put the work together. To do so, I could 'merge' branch2 into branch1 - and viola, branch1 now contains the changes to homepage.html *and* the changes to subpage.html
- *Fetch*: Getting the latest versions from remote repositories without merging them into your current work.
- *Pull*: To fetch, then merge, work into your current branch. You pull to take someone else's work from a remote repository.
-- For example, assume I edit homepage.html on branch1, and my coworker edited subpage.html in *his* repository. I could fetch his branch from his repository, then merge it into mine - or I could simply 'pull' his branch, which would automatically fetch and then merge it into my current branch.
- *Push*: You push to send your work to a remote repository.
-- For example, assume I edit homepage.html, and my coworker wants to finish my work. I can push my work to github, so that my coworker can find, and then pull, my recent work.

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
