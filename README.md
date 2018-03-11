# Git Commands!

### 1. git clone:

    Clones the git repo to you local.
    git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git
    
### 2. git status:

    Tells if any file that git repro has be modified and if the repo is uptodae with the master.
    git status

### 3. git commit:
    
    Commits changes to the git repro. 
    git commit -a -m "Message that needs to be added along with the commit"
    -a --> Add all files to commit from staging.
    -m --> Message to be added to the commit.
    
    git commit --list
    Gives the config for the git repro in our local machine.
    
### 4. git remote:
    
    Lists all the remote project
    remote is the clone instance of the master branch/ master branch 
    git remote -v
    -v --> is also given the url link of the git repo.
    
    eg: origin	https://github.com/nchandar/practice-programming.git
    origin -> remote (for some reason the default name of the first remote is always origin, we can have other names as well).
    -v -> verbose returns the URL.

### 5. git push:
    


### 5. git commit:
    
    Commits changes 
    git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git

### 1. Clone your fork:

    git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git

### 2. Add remote from original repository in your forked repository: 

    cd into/cloned/fork-repo
    git remote add upstream git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git
    git fetch upstream

### 3. Updating your fork from original repo to keep up with their changes:

    git pull upstream master

