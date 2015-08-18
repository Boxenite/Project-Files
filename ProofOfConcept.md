## PoC

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
box command connects you to sftp service
we represent your projects as a file directory, navigate to your project
launch cd into your project actually connects you sftp directly to your dev machine



can you build a command line tool that reroutes all requests in a given directory to a remote server? 


use a dedicated dropbox folder? keep one on the remote server, one on the local computer? 

possible flow for local and remote 

1. user auths into boxenite using dropbox auth
2. 
