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
- *Commit*: A commit (revision) is a change to a file or set of files which is saved to git's history. A user must 'commit' changes they made for git to track them. Commits are tracked with a unique ID (the "SHA" or "hash"), an author, a time, and, usually, a description of the changes.
- *Branch*: A 'version' of a repository. Branches exist in parallel. Unless explicitly merged, work on each branch remains unaffected by work on other branches.
- *Tag*: A 'snapshot' of a repository at a certain point in time.
- *Checkout*: Checkout is a command used for switching to a different branch (version) of the same repository.
- *Fork*: A personal copy of a repository. If you see a repository you want to work on, you can fork (copy) it, and make all the changes you want to your forked copy.
- *Merge*: To combine work from another source (e.g. version, branch, or commit) into your current branch.
 - For example, assume I edited 'homepage.html' on my branch1, and subpage.html on my branch2. I now want to put the work together. To do so, I could 'merge' branch2 into branch1 - and viola, branch1 now contains the changes to homepage.html *and* the changes to subpage.html
- *Fetch*: Getting the latest versions from remote repositories without merging them into your current work.
- *Pull*: To fetch, then merge, work into your current branch. You pull to take someone else's work from a remote repository.
 - For example, assume I edit homepage.html on branch1, and my coworker edited subpage.html in *his* repository. I could fetch his branch from his repository, then merge it into mine - or I could simply 'pull' his branch, which would automatically fetch and then merge it into my current branch.
- *Push*: You push to send your work to a remote repository.
 - For example, assume I edit homepage.html, and my coworker wants to finish my work. I can push my work to github, so that my coworker can find, and then pull, my recent work.

### Git Workflows
Git is especially useful, and necessary, on large projects. But using git alone is not enough - team members need to be on the same page in *how* they use git. Our preferred git workflow is called 'Git Flow'.

#### Git Flow
'Git flow' defines a process team members must follow when writing code for the production (aka prod) website.

##### Rules
1. The 'master' branch contains work that has been (or is currently being) released on prod.
2. The 'develop' branch contains work that the team plans to release to prod.
3. Work (tasks/features) currently being developed should reside on feature branches based on the develop branch.
4. Every new task/feature should be on its own feature branch.
5. Individual feature branches should be merged into the develop branch *only after being reviewed and approved for prod*.
6. The develop branch should be merged into the master branch *only when the develop branch's work is released on prod*.

##### Example
We are a team with 5 developers working on debugacademy.com , using git flow.
- The prod website's code matches the 'master' branch exactly.
- The develop branch has a project management module on it, waiting to be deployed.
- Ashraf will now begin working on a user dashboard page, complementary to the project management module.
 - Ashraf will create a new *feature branch* based off of the develop branch
 - Ashraf will name the new branch something unique, such as 'pm-user-dashboard'
- When Ashraf finishes his work, he creates a pull request for his feature branch
- After a coworker (and client, if applicable) has reviewed and approved the work:
 - A senior team member will merge the work into the develop branch
- When the work on the develop branch is ready to be released on prod:
 - The develop branch will be merged into the master branch
 - Prod will be updated to match the master branch

### Your first Git repository
We have a repository (repo) named 'assignments'. This repo will contain a number of assignments for getting you up to speed with Git, as well as other technologies.

#### Getting started with the assignments repo
0. Log in to github.com
1. Fork the debugsociety/assignments repo on GitHub
2. Copy the HTTPS clone URL from your forked assignments repo
- For example: https://github.com/YOUR-GITHUB-USERNAME/assignments.git
3. In the terminal, cd to the directory you want to place the repo folder in
4. Clone (copy) the repo into that directory using the git clone command: "git clone URL-OF-FORKED-REPO"
- For example, git clone https://github.com/YOUR-GITHUB-USERNAME/assignments.git

##### Set up your repo's remote connections
If you followed the steps in the previous section, then you have cloned your fork of the assignments repo. Great - now we have a copy of the entire repo on our computer. What next?

###### Why?
Ultimately, we want to share our work with teammates (PUSH), and we want to be able to take work that they have shared (PULL). Where do we want to push to? Where do we want to pull from? These are our 'remote' repositories.

###### How?
Type 'git remote -v' to see which remotes you are currently connected to. By default, you are only connected to the remote which you cloned the repo from, and it is named 'origin' by default. In this example, you should see the URL to your forked 'assignments' repo.

Your fork is where you can push your work to. What if the official repo is updated? We want to be able to pull the latest updates from that repo.

Let's set ourselves up to be able to pull work from the official repo:
1. Go to the official assignments repo
- Found at github.com/debugsociety/assignments
2. Copy the HTTPS clone URL from that repo
3. cd to your local assignments repo
4. Add the official repo as a remote: git remote add [alias] [URL]
- For example, to name the connection 'prod', you would run the following: git remote add prod https://github.com/debugacademy/assignments.git
