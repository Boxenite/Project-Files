## Concept
Devbox - private, hosted development servers for every engineer. Simple to spin up new environments, whether it is off the shelf containers from google or Docker, to recipes from Chef, to your own favorites, or a CLI creation flow. 

The use of Dropbox and Git seems extremely popular. http://stackoverflow.com/questions/1960799/using-git-and-dropbox-together-effectively

## Feasibility
* [Here is a guy at thoughtbot building his remote dev server](https://robots.thoughtbot.com/remote-development-machine)
* SSHFS - mounting filesystems from a remote server - so you don't have to copy files locally to edit with popular editors
  *[using fuse - may not work with atom](http://osxfuse.github.io/)
  *[another solution macfusionapp](http://macfusionapp.org/)
  *[atom.io discussion](https://discuss.atom.io/t/working-with-ssh/1737/11)
  * [Linux file system (FUSE) to access Dropbox, Sugarsync, Amazon S3, Google Storage, Google Drive](https://github.com/joe42/CloudFusion)
  * [sshfs digitalocean](https://www.digitalocean.com/community/tutorials/how-to-use-sshfs-to-mount-remote-file-systems-over-ssh)


## Market Research

Workflow products for setting up development environments remotely and connecting to them
* [Vagrant](https://www.vagrantup.com)

Infrastructure as code solutions are recipe based containers that are not made to spin up on VMs, but rather on optimized linux boxes. Existing Infrastructure as Code solutions:
* [Docker](www.docker.com)
* [Chef](https://www.chef.io/chef/)
* [CoreOS](https://coreos.com)
* [Kubernetes - google container engine](http://kubernetes.io/)

Cloud Hosting for Developers
* [Digital Ocean - simple cloud hosting for developers](https://www.digitalocean.com)
* [Heroku - cloud application platform](www.heroku.com)
* [bitnami - vm app hosting](www.bitnami.com)
 
Browser based IDE
* [codeanywhere](https://codeanywhere.com)
* [nitrous](https://www.nitrous.io)
* [cloud9](https://c9.io)
* [codenvy](www.codenvy.com)
