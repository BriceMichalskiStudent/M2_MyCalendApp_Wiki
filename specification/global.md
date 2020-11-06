[MyCalendApp](../README.md) > [Spécification](./specification.md) > [Global Specification](./global.md)

# I - Global Specification

## 1 - Origin of the need

The MyCalendApp project addresses the need for online event organization, discovery and management. The calendar orientation of this project will allow it to group on a single page upcoming events, accept, refuse or send invitations. A chat linked to each event will allow the participant to organize himself there, as well as to visualize all the information related to the event. 

## 2 - Dictionary

...


## 3 - Objectives

### General Goals

The main objective of the MyCalendApp project is to provide a platform to simplify the organization of events. 
As well as to allow users to better organize their time.

### Functional Goals

Each user will have to be able to:
- Create, edit, delete, invite, make public or private an event
- Join , leave, consult a list of public or private events to which he has been invited
- Added friends to be able to view the public events in which they participate.
- discuss, access to images and information on the events to which he or she subscribes

### Secondary functional Goals

Each user will have to be able to:
- Subscribe to tags and thus be kept informed when creating events containing this tag.
- The user must be able to connect through his facebook account and see his facebook events on his MyCalendApp calendar.

### Targets
Will be targeted by this application :
- A young population adept with online digital tools
- People with a wider circle of friends who have organizational difficulties
- Older people with memory loss

## 4 - Quality of Service and Security

### Availability 

The availability of this application will depend on the availability of the Heroku cloud provider, refer to [Heroku Status Page](https://status.heroku.com/).

### Security

All connections to the MyCalendApp application will be made via the HTTPS protocol. A dependency security analysis is also implemented by github via [Dependabot](https://docs.github.com/en/free-pro-team@latest/github/managing-security-vulnerabilities/about-alerts-for-vulnerable-dependencies).

The authorizations will be done via a JWT and the login will be done via a database encrypted password.

## 5 - Delivery

Delivery to production will be done automatically when merged to master according to GitFlow Workflow.

It can also be done on demand by the development team.