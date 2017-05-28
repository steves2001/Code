#Setup

## Sign up of github

* create an empty repository
* 

##Go to local development machine 

* Start Git bash shell
* start virtual machine
** type vagrant up
* open a secure shell to the virtual server
** type vagrant ssh
* cd to code folder
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
