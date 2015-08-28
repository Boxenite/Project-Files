# Boxenite
###development servers that don't suck
* code syncing between multiple devices
* store code locally
* deploy local
hr
* store code locally
* deploy remote
* 

* store code locally or on your development server (hello enterprise - give me your money)
* Easily share your development
* Add-on Services
  * DB Proxy - easily control what databases and queries are allowed by your development servers
  * CI for all development servers
  * Slack, of course.

Problem: Configuration work is a hassle and small differences create large problems. Sharing configuration takes work that should be already built into your minimal workflow. 
Why can't I pull any repo and start working on it immediately without having to configure my machine? 
I could use things like vagrant, but why isn't this shit just happening automagically? 
but then my database doesn't have any data in it. 
The sharing mechanism needs to already do the dirty work and live natively inside my workflow


today's workflow for a project
* clone repo to local
* install dependencies (WOOF can be a big step)
* install server
* create DB, migrate DB
* run


Tomorrows Workflow
* clone development server
* run


## Keys to Growth
* Free for open source projects
* can be used immediately inside companies and for individuals
* A-ha moment - your development server is hooked up to a development database... that already has data in it! cloning also replicates the development db or allows you to connect to one development db shared by all clones

## Use Cases
* saw a cool project on github, want to clone and start messing around with it
* want to contribute to an open source project
* want to reduce conflicts due to different environments
* new engineer on a project and want to dive in immediately
* I want to develop and test using production data, safely
* I want people to contribute to my open source project
