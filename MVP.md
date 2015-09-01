###Boxenite

**Configuration - only if you want to.**
Vagrant, Docker, etc. - they all are fantastic tools but lack a simple experience that impacts enterprise users and individual engineers. We are going to backdoor this product into every enterprise because it will be THE way engineers start, collaborate and work on their projects.

**MVP - Development Servers that Just Work**
* Adding a project or file to your Boxenite Folder creates a remote development server. 
* remote development server stays in sync with your local folder. it effectively becomes your local.
* to the user, EVERYTHING must feel like they are running it on their own machine. Absolutely no learning curve. 
* cloning repository to your boxenite folder is the only action you have to take to get up and running
* support 1-2 most popular project types
* Free to use for development (we will eat the cost on MVP)
* easy to share your exact environment - we guarantee consistency in environments when you share your projects
* **unlocks:** Use Case 1,2,3,4

**Things we abstract away**
* installing dependencies locally for every new project 
* setting up account and server on digitalocean, heroku etc. 
* writing configuration files

###V1
* code syncing between multiple devices
* database cloning - fire up an existing project with a populated db, if the project owner has one

###V2
* code is remote
###Important to the Model
* forever free for open source
* private repositories come at a cost

###Use Cases
1. I want to share my project with someone else
2. I want to invite someone else to my project and to my development server environment (database included)
3. I want to jump into a new project without dealing with dependencies
4. I want to share my development or production configuration and integration testing to anyone or specific people
5. I want my code synced across my different computers
6. I want people to contribute to my open source project

Problem: Configuration work is a hassle and small differences create large problems. Sharing configuration takes work that should be already built into your minimal workflow. 
Why can't I pull any repo and start working on it immediately without having to configure my machine? 
I could use things like vagrant, but why isn't this shit just happening automagically? 
but then my database doesn't have any data in it. 
The sharing mechanism needs to already do the dirty work and live natively inside my workflow


**today's workflow for a project**
* clone repo to local
* install dependencies (WOOF can be a big step)
* install server
* create DB, migrate DB
* run

**Tomorrows Workflow**
* clone development server to your boxenite folder
* run

## Keys to Growth
* Free for open source projects
* can be used immediately inside companies as is (exception being on-prem enterprise)
* is valuable enough to individual developers to adopt it into their workflow
* A-ha moment - your development server is hooked up to a development database... that already has data in it! cloning also replicates the development db or allows you to connect to one development db shared by all clones



