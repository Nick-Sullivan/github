#####################
# Cheat sheet not listed elsewhere
git checkout -b branchname    Creates a new branch
git diff branch1..branch2     Displays differences between branches

#####################
# Initial setup
Git needs to be installed.
  sudo apt-get install git
Then we set details of the GitHub user.
  git config --global user.name "Nick Sullivan"
  git config --global user.email nick.dave.sullivan@gmail.com
You can view the details.
  git config --list
Set the password cache.
  git config --global crediential.helper "cache --timeout=3600"

#####################
# Creating a repository locally
Set folder as a repository
  git init
View files being tracked
  git status
Add files to be tracked (staging)
  git add (-A for all, -u for detected changes)
Commit changes
  git commit -m "Message"
  
#####################
# Creating a GitHub repo from a local repository
Click + to add a new repository
Create without a README
Push an existing repository from command line
  git init
  git add -A
  git commit -m "first commit"
  git remote add origin https://github.com/Nick-Sullivan/testrepository.git
  git push origin master

#####################
# Creating a local repository from a GitHub repo
Set folder as a repository
  git init
Set it to the online repo
  git remote add origin https://github.com/Nick-Sullivan/testrepository.git
Fetch repo info
  git fetch
Choose branch
  git checkout master
Get files from the cloud
  git pull

#####################
# Everyday operations
Update the local copy of the cloud (does not change our files)
  git fetch
Display list of branches
  git branch
Change into desired branch (changes local files to the local branch)
  git checkout mybranchname
Download branch contents from the cloud (changes local files to match cloud)
  git pull
Make changes to files
Check all files are tracked
  git status
Add all changed files
  git add -u
Check changes
  git status
Commit changes
  git commit -m "message"
Push changes to cloud
  git push origin branchname
Possibly pull request, merge, delete repositories
  (do it online in GitHub.com)
Update the local copy of the cloud 
  git fetch
  git checkout master
  git pull
Remove a local repository
  git branch -d mybranchname
  
#####################
# Debugging
View the commit log
  git log
Checkout to a previous state (can't commit changes)
  git checkout unique_id
Remove git tracking from a folder
  rm -rf .git

