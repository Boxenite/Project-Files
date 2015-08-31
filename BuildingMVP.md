##Building the MVP

####MVP
* CLI that creates a remote server (that can compile build and run) for any directory in the boxenite folder
* server code that can understand dependencies, create and launch the correct container on cloud hosting platform
* account creation, login, deletion
* easy share to an email

###Components
* Digital Ocean is the hosting platform
* ruby api for creating their containers (droplets)
* server - for managing the server provisioning, accounts
* command line tool / syncing service for live updates to running server


### These are just notes

* folder syncs with server
* can set up folder on many computers
* can use git / subversion on server
* run / start commands creates a remote container and runs it
* any updates to the code locally will reflect in the server and in the live container if possible


* remote environment is accessible to editors locally without the files locally
  something like http://www.expandrive.com/apps/expandrive/ crossed with dropbox
* 

### Prototype feature list
* adding a project to the folder creates the remote environment
* remote environment is accessible to editors locally
* command line commands in the folder directory are actually running on remote server

command line tool: $user: box command connects to the service and changes your directory to your boxenite folder, with optional auth / 2 fac
- all subsequent commands while in box should run in the boxenite system (server) (think sftp)
- box exit should drop out of your box experience
- build new project directly in box - should support popular framework commands


possible tech solutions: 
boxenite folder is a parent directory that is a collection on remote environments represented by a folder for each environment
cd into each folder connects you directly to that project
