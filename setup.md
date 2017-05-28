# Setup

## Sign up of github

* create an empty repository
* make a note of the repository address https://github.com/steves2001/Code.git

##Go to local development machine 

* Start Git bash shell
* start virtual machine
** type vagrant up
* open a secure shell to the virtual server
** type vagrant ssh
* cd to code folder
* git config --global user.email "me@stephensmith.me.uk"
* git config --global user.name "Stephen Smith"
* type git init
* type git add .
* type git commit -m "First commit"
* type git remote add origin https://github.com/steves2001/Code.git
* type git remote -v
* type git push origin master

## To copy repository to remote server

* Login to server using putty
* type mkdir repos
* type mkdir Code
* type mkdir repos/Code
* type cd repos/Code
* type git clone https://github.com/steves2001/Code.git

## To copy site files to the servers web folder

* type git checkout-index -a -f --prefix=/kunden/homepages/43/d520356031/htdocs/Code/

## Update github with changed files

* git add .
* git commit -m "Instructions added"
* git push origin master

## Retrieve updates from github

*Solution 1: no conflicts with new-online version

git fetch origin
git status
will report something like:

Your branch is behind 'origin/master' by 1 commit, and can be fast-forwarded.
Then get the latest version
git pull
*Solution 2: conflicts with new-online version

git fetch origin
git status
will report something like:

error: Your local changes to the following files would be overwritten by merge:
    file_name
Please, commit your changes or stash them before you can merge.
Aborting
Commit your local changes

git add .
git commit -m ‘Commit msg’
Try to get the changes (will fail)

git pull
will report something like:

Pull is not possible because you have unmerged files.
Please, fix them up in the work tree, and then use 'git add/rm <file>'
as appropriate to mark resolution, or use 'git commit -a'.
Open the conflict file and fix the conflict. Then:

git add .
git commit -m ‘Fix conflicts’
git pull
will report something like:
Already up-to-date.