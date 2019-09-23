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
    
    git remote add (remote name eg: origin or any name) (remote url)
    This add a new remote to our local.
    eg : git remote add origin https://github.com/nchandar/practice-programming.git
    instead of origin as remote name, we can have any name in there.

### 5. git push:
    
    Pushs changes from the local git repo into the remote & branch which needs to be specified along with this command
    git push (remote) (master)
    eg: git push origin master
    origin -> remote
    master -> branch

### 6. git fetch:
    
    It is same as Pull, but it won't do any merging. So you can carefully monitor the files before merging it.
    git fetch origin master
    
    (also see rebase if needed)

### 7. git pull:
    
    Pulls down from a specified remote (Specified by the user) and will instantly merge it into a branch we are present on. It is basically a mix of Fetch and Merge commands.
    git pull master origin

<br />
<br />
<br />

## Commands to create git repo locally and push it into github.

### 1. git init:
    
    In the directory where all the files are, if this command is executed thenit creates a new git repo locally.

### 2. git add:
    
    Adds all the files that were initialised to the staging area.
    git add (file name) --> if a single file needs to be added.
    git add .  --> for all the files to be added.
    
### 3. git commit:
    
    Here we just need to commit right away and we don't need to add (-a) as it has already been added.
    git commit -m "Message for commit."
    
###### Till here the changes are not committed to the github all the canges are still in local git repro.
###### Create a git repo in the github website.

### 4. git remote add:
    
    If the remote is not added add a new remote.
    git remote add newOrigin git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git
    
### 5. git push:
    
    Push all the changes from local machine into the new github repo that was created.
    git push newOrigin master

<br />
<br />
<br />

## Commands to update a for that we have in github.

### 1. git commit:
    
    Commits changes 
    git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git

### 2. Clone your fork:

    git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git

### 3. Add remote from original repository in your forked repository: 

    cd into/cloned/fork-repo
    git remote add upstream git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git
    git fetch upstream

### 4. Updating your fork from original repo to keep up with their changes:

    git pull upstream master

<br/>

## How to update a forked repo with git rebase :

### Step 1: Add the remote (original repo that you forked) and call it “upstream”

    git remote add upstream https://github.com/original-repo/goes-here.git

### Step 2: Fetch all branches of remote upstream

    git fetch upstream

### Step 3: Rewrite your master with upstream’s master using git rebase.

    git rebase upstream/master

### Step 4: Push your updates to master. You may need to force the push with “--force”.

    git push origin master --force

<br/>
