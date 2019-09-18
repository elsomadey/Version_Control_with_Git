# Version_Control_with_Git

## What is GIT
Git is a version control system, a tool that tracks changes to
your code and shares those changes with others. Git is most useful
when combined with GitHub, a website that allows you to share your
code with the world, solicit improvements via pull requests and track
issues.”

## Why do we need to use GIT
We all can be agreed in a point that it is absolutely important to
collaborate in a project for better outcome. Git or any other version
control is the best way to track your code and work with the other
people. Here are some more reasons why one should use Version Control System:
  * Collaboration
* Storing Versions (Properly)
* Restoring Previous Versions
*  Understanding What Happened
*  Backup

## How to start using GIT

* Download and install GIT in your computer.

* Create an account in GitHub or BitBucket. Once created open the account with your username and password.

* Create a New Repository in GitHub from the '+' sign on the right hand side of the page.
  * Write Repository Name
  * Add description about the repository content
  * Now select 'Public' - if you want everyone to see your repository or 'Private' - if you want selected people to see your repository.
  * Check box ' Initialize this repository with README
  * Click 'Create repoitory'
* Create a folder in your computer where you want to create the files. Go within that folder. 
  * Write cmd in the address bar. A window will open.
  * Write 'code .' beside the blinker and press enter. - Visual Studio Code will open.
  * Go to 'Terminal' - 'New Terminal'. Git will open below.
* OR we can right click on the folder and click 'GIT Bash Here' - GIT Bash will open and there we can write the commands

## Basic GIT Commands


```bash
#   To check the version of GIT

$ git --version

#  Set GIT username

$ git config --global user.name "elsomadey"

#    Confirm that you have set the username corretly

$ git config --global user.name
> elsomadey

#    Set GIT email

$ git config --global user.email "elsomadey3@gmail.com"

#    Confirm that you have set the email corretly

$ git config --global user.email
> elsomadey3@gmail.com

#   Print out the location of the current directory.

$ pwd 

#   Creating new directory

$ md directory_name

#   Entering into the current repository.

$ cd Version_Control_with_Git/

#   Getting out of the current directory

$ cd ..

#   Listing the files in the current repository or directory

$ ls

#   Creating files with different extension (eg .doc, .txt, .md, .py etc) in the current repository.

$ touch README.md 

#    Add all the files in the local repository and stages them for commit

$ git add .

#   Add a specific file in the local repository and stages them for commit

$ git add README.md

#   Create empty Git repo in specified directory. Run with no arguments to initialize the current directory as a git repository.

$ git init <directory>

#   Checking the status of all the files  to be committed

$ git status

#   Commenting on what changes made so that other users can get an idea of it.

$ git commit -am "First commit"

#   Uncommit changes just made to the GIT repo

$ git reset HEAD~1

#   Pushing the changes made to the local repo to the remote repository in GitHub

$ git push origin master

#   Pulling any file from remote repository.

$ git pull URL_address

#   To check the difference between two files.

$ git diff file1 file2

#   Revert back to the last committed version to the Git Repo

$ git checkout .

#   To see the history of commit made to the files

$ git log

#   Cloning a Git Repository:
First locate the repo in GitHub you want to clone, copy the URL of the repo. then write the command: 

$ git clone remote_repository_URL
```

## Branching in GIT:
Branching is a feature available in most modern version control systems. Git branches are effectively a pointer to a snapshot of your changes.

#### Why branching is required?

* When you want to add a new feature or fix a bug, it is not recommended to do do changes directly to master branch(Main branch) to avoid the chances for unstable code to get merged into the main code base. So, you can create a new branch to encapsulate your changes.

* It becomes convenient to work with multiple members in a team when each member is working on their own branch and when the code is tested to be working fine; branches can be merged to the main branch.

#### Branching Commands in GIT
```bash
#   List all of the branches in your repository

$ git branch

#   Create a new branch called B_1 and enters into the branch

$ git checkout -b B_1

#   Switching branch

$ git checkout branch_name

#   Delete the specified branch. But Git prevents you from deleting the branch if it has unmerged changes.

$ git branch -d B_1

#   Force delete the specified branch, even if it has unmerged changes.

$   git branch -D B_1

#   Rename the current branch

$ git branch -m B_2

#   List all the remote branches

$   git branch -a

#   Creating a remote branch

$ git remote add remote_branch_name remote_branch_URL
$ git push remote_branch_name local_branch_name~

#   To delete a remote branch

$ git push origin --delete remote_branch_name

#   Merging specific branch to current branch

$   git merge branch_name
```
## Merge Conflict
The main reason of merge conflict is that there are different changes in the same line(s) of a file(s) in the branches that are to be merged. So, when there is a merge conflict, you have to decide on which clashing line(s) should have what code.


In my opinion, always work on a branch even if the feature is trivial. Keep rebasing it as you feel like, depending upon the frequency of the team that is commiting to the project. Afterwards create a PR to merge it with the main branch or master.


## Git Stash
Git follows a 2 step commit process and staging a files for commit is the first step. The second being actually committing those files.

You can selectively stage files for commit using 
```bash
$ git add <filename>
```

Git stash is a way where you can stash your changes if you are going to be changing branches.

Suppose you are working on a branch and has a lot of local changes and you want to switch branch and port all these local changes.

You could do
```bash
$ git stash
```
Switch branch do whatever and when you are ready to bring back your changes just do
```bash
$ git stash apply
```


## Generate/check your machine for existing SSH keys.
 Secure Shell (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network.
 Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect to GitHub without supplying your username or password at each visit.

```bash
#   to see if existing SSH keys are present:
$ ls -al ~/.ssh
```
 Lists the files in your .ssh directory, if they exist.

 To create new SSH keys follow the link below:
https://www.youtube.com/watch?v=-ElU6WhNLn4