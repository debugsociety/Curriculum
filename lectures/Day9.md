Discussed steps and commands for Git
Git init: 
- is for creating a new git repository. It turns the current directory into a git repository. 


git clone: 
- is adding the files to your (physical) computer
- is for copying (aka cloning) an existing git repository
- For example git clone https://github.com/debugsociety/Curriculum.git curriculum downloads a copy of the entire Curriculum repository into a local folder (on your computer) called 'Curriculum'


git add: 
- Git will include the 'add'ed files into your next commit.
- Files that were not added will remain untracked by git. 
- Make sure you add the file exactly as is.
- For example: if it has Day1.md, write git add Day1.md

git commit: 
- Git commit will save the current version of all files that were added using 'git add' to history.
- Before and after meaningful changes are made, there should be a commit.
- Git commit -m "". Add a message within the ""
- If this message displayed: no changes added to commit
- You must git add [the file] then commit 

git checkout -b:
- Git checkout -b is when you want to create a new branch and switch to that branch.
- For example, I want to create a new branch named hello, I'd write git checkout -b hello
- Then it should tell you that you are on branch hello

git checkout [branch] : 
- Git checkout means that you are switching branches. 
- For example, I am on branch hello and now I want to switch to the master branch.
			- write git checkout master


git remote add [url]:
- Git remote add, adds a connection to a repository.
- For example:
	-git remote add https://github.com/debugsociety/Curriculum.git


git remote:
- Shows which nicknames of the remote repositories that you are connected to.
- For example, 
		-git remote might display: debugsociety origin

git remote -v:
- shows you the entire link of the repositories 
- For example,   
		debugsociety   https://github.com/debugsociety/Curriculum.git (fetch)
		debugsociety   https://github.com/debugsociety/Curriculum.git (push)
		origin    https://github.com/..[yourgithub]/Curriculum.git (fetch)
		origin    https://github.com/..[yourgithub]/Curriculum.git (fetch)

git branch:
- Shows you all the branches on your computer with an asterisk next to the branch you are on.
- For example,
		 master
		*branch2

git push [name of repository] [branch you are pushing]:
- Git push is when you want to send it to the online repository 
- Git push is sending the entire branch 
- For example, 
		- git push debugsociety branch2 

git pull : 
- Git pull means that you are extracting any new changes into your branch
- When you git pull, must be in the correct branch that you want to pull into
- For example, if I want to pull from debugsociety's 'master' branch into my 'branch2' branch
		-git pull debugsociety master

git merge:
- Git merge is when you want to bring commits from a local branch into the current branch
- For example, if I have branch2 and branch4 in my local repository and I want to bring the changes from branch4 into branch2
		 -git checkout branch2
		 -git merge branch4




