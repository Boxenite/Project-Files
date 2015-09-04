# Architecture

Minimum viable proof of concept, essentially [BuildingMVP](BuildingMVP.md).

## Theory of Operations (bit of CONOPS for flavouring).

This section assumes a fully onboarded and commited user. Funneling, conversion
and such are out of scope, even though they will drive design decisions; however
in the absence of data, it would be premature to assume all use cases.

The product (hereinafter, boxenite) is the confluence of 7 major components,
separated into the traditional backend and frontend systems.

The frontend is responsible for providing system services, sheparding
user actions and funneling experiences while the backend has the responsibility
to provide robust operations, security and availability.

Component details at eleven.

Assumptions:
- only self contained trivial projects, i.e. well known stack
  - edit / test cycle, no compile.
  - Basic side kicks though, e.g. postgres, redis
- Existing project in VCS, i.e. git
- commited user, i.e. fully configured client, functioning backend.
  - service directory
  - auth^2

```bash
: user@laptop ~ $; boxenite init && eval $(boxenite env)
...
: user@laptop ~ $; cd $BOXENITE_DIRECTORY
: user@laptop ~/$BOXENITE_DIRECTORY $; git clone git://git@github.com/user/proj.git
...
: user@laptop ~/$BOXENITE_DIRECTORY $; cd proj
: user@laptop ~/$BOXENITE_DIRECTORY $; boxenite up
instanceid: guid
www: https://instanceid.boxenite.tld/
console: https://instanceid.boxenite.tld/console
ssh: ssh://user@instanceid.boxenite.tld
: user@laptop ~/$BOXENITE_DIRECTORY/proj $; $EDITOR file
... edit / test / sync / rinse / repeat
: user@laptop ~/$BOXENITE_DIRECTORY/proj $; boxenite share <user|public>
https://instanceid.boxenite.tld/?data=<base64chunk>
: user@laptop ~/$BOXENITE_DIRECTORY/proj $; boxenite destroy
...
```
XXX(thorduri): boxenite v. git bxe (a la github = git + hub).

## Logo Slide
`cloud`, `containers`, `devenv-as-a-service`

## Components

What follows is the general outline of responsibilities of each component,
their interactions and overall architecture.

### Frontend

A key design aim should be service statelessness, i.e. it's recreateable
from the backend system.

#### Web

Essentially the boxenite site, signups, marketing, branding all that jazz.

Feature parity with app is not essential, but basic tasks should be possible,
such as destroying, unsharing, changing password, audit logs etc.

#### App

Think `Postgres.app`.
A "Command & Control" center.

#### CLI

All functions of the app are done via the CLI either on behalf of the
user or user initiated.

#### Daemon

Responsible for monitoring the BOXENITE_DIRECTORY, life cycle management of
instances, re authentication (changed network), resync, teardown/boostrap in
face of errors etc.

### Backend

Responsible for all product services that are not user actions, but servicing
those.

#### API

Essentially the product, everything happens one way or another through the API.

"HTTP/REST^WRPC", however we should allow for binary protocols from the get go.

#### Provisoner

Main service, responsible for management of instances, their boostrap/teardown,
service discovery etc.

#### Infrastructure

Essentially, every project is a data container, that holds the git repository,
syncronization is done via git OR filesystem changes (yay, let's reinvent dropbox).

We assume that we can run the project in a container, e.g. docker but this places
serious constraints on service levels.

An instance is essentially a docker container, the Provisoner is responsible for
it's life cycle management and security while the API provides access to it, along
with the ,,views''.
