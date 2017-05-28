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

*