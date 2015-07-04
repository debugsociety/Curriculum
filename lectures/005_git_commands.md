# Git
Git is a Version Control System, or 'VCS'. It takes snapshots of the state of files when changes are made. It is extremely beneficial and necessary on any large software project.

## Git Settings and Configuration
#### Installation
Follow installation instructions here:
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

#### Setup
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR EMAIL ADDRESS"

#### .gitignore
You can add a .gitignore file to your project/repo's root directory to specify which files and folders git should NOT track. For example, you likely do not want to track files which contain sensitive information, such as the database's username and password, in a public repo.

See http://git-scm.com/docs/gitignore for more information.

## Commands for Git
#### git init:
- For creating a new git repository.
- It turns the current directory into a git repository.
- For example:
-- 'cd' into a non-git folder.
-- Type 'git init'.
-- Now the folder is a git repository.

#### git clone [URL] [destination-name]:
- For copying (aka cloning) a repo (and all files in it) from a URL to your computer.
- For example:
-- "git clone https://github.com/debugsociety/Curriculum.git curriculum_local"
-- That will download a copy of the entire Curriculum repository into a local folder (on your computer) called 'curriculum_local'

#### git add [file or folder]:
- Includes the 'add'ed files *in your next commit*.
- Changes to files that were not 'add'ed will remain untracked by git.
- Filenames must be typed exactly and with extensions.
-- For example, if you want to add a file named File1.html to your next commit:
-- git add File1.html will work.
--- 'git add File1' will NOT work.
--- 'git add file1.html' will NOT work.

#### git commit -m "[message]":
- Stores the current version of all files that were added using 'git add'.
- There should be a commit for every meaningful change.
- There should be a short message describing what the commit is for.
-- For example: git commit -m "Updated git_commands.md"
- If this message displayed: no changes added to commit, it means you did not 'git add' your changes before committing them.

#### git checkout [branch] :
- Used to switch branches.
-- For example:
--- I am on the 'master' branch
--- git checkout hello-world
--- If it exists, I am taken to the branch named 'hello-world'

#### git checkout -b [new-branch] [branch]:
- Used to create a new branch named [new-branch], which initially matches the branch named [branch] exactly
-- For example:
--- git checkout -b my-branch master
--- The branch 'my-branch' is created based off of the 'master' branch
--- Then I am taken to the new 'my-branch' branch

#### git remote add [alias] [url]:
- Adds a remote connection to a repository.
- For example:
-- git remote add ds https://github.com/debugsociety/Curriculum.git
-- Now we are connected to (can pull from) the 'debugsociety/Curriculum' repo.
--- If we have the right privilidges, we can also now push to the 'debugsociety/Curriculum' repo.
-- i.e. git pull ds master ## this command will now automatically pull from debugsociety/Curriculum.git

#### git remote:
- Shows the nicknames of the remote repositories that your repo is connected to.
-- For example:
-- git remote might display:
--- - origin
--- - ds
- *Passing the -v flag shows more detail.*
-- For example:
-- git remote -v might display:
--- - ds   https://github.com/debugsociety/Curriculum.git (fetch)
--- - ds   https://github.com/debugsociety/Curriculum.git (push)
--- - origin    https://github.com/[YOUR-USERNAME]/Curriculum.git (fetch)
--- - origin    https://github.com/[YOUR-USERNAME]/Curriculum.git (push)

#### git branch:
- Shows you the branches on your computer
- Places an asterisk next to the branch you are on.

#### git branch [name]:
- Creates a new branch named [name].
- The new branch's history matches the branch you created it from.

#### git push [remote] [branch you are pushing]:
- Used for sending commits from [branch] to [remote]/[same branch]
- Sends ALL committed work on [branch you are pushing]

#### git merge [branch name]:
- Merges work from [branch name] into the branch you currently have checked out.
- For example, if I have branch2 and branch4 in my local repository and I want to bring the changes from branch4 into branch2
  - git checkout branch2
  - git merge branch4
- If it says 'merge conflict', that means the two branches make changes to the same section of the same file
-- Git will insert the changes from BOTH branches in the file
-- Git will insert '<<<' within the file(s), before each conflict
-- Git will insert '>>>' within the file(s), after each conflict
-- It is your job to review what git has added to the files, then to remove what you do not want. Such as '<<<' and '>>>'.
-- After resolving the conflict, it is your job to add and commit your changes.
-- Following git workflows such as 'git flow' minimize messy merge conflicts.

#### git pull [remote] [branch name]:
- Immediately/automatically merges all new changes from [remote]/[branch name] to the branch you currently have checked out.
- When you git pull, make sure you have the branch you want to pull into checked out
- For example, if I want to pull from debugsociety's 'master' branch into my 'branch2' branch
    - git checkout branch2
    - git pull debugsociety master
