# cloud.gov notes

## Summary

Notes on Cloud.gov

## Introduction

* Codez - https://github.com/dlapiduz/workshop

### Meaning of Cloud Native/Cloud Ready

* Started as cloud project?   No.
* 12-factor app - built to be automatically provisioned among other things.

### How to get to Cloud Native/Cloud Ready:

* Microservices
* Queues between services
* ... consult 

### What is cloud.gov?

__NOTE:__ Running Cloud Foundry (Pivotal?) but branded as cloud.gov

* PaaS
* Ruby, Java, PHP, Go, Clojure, Meteor, Node.js, Python and others
* Shared services - mysql, postgresql, redis, elasticsearch
* Built-ins - logging, auditing, authentication and permissions are built-in (to what extent?)
* Common compliance up to the application layer
* Some concepts:
  - Organization, space, application, instance
  - Buildpack
  - Services / Marketplace

### How do I use it?

__NOTE:__ demo by Aiden

* Create an account - we should receive an invitation to a Sandbox account, but can try at other CloudFoundry implementations.
* Download cf cli - https://github.com/cloudfoundry/cli (releeases) and note also https://docs.cloudfoundry.org/devguide/installcf/install-go-cli.html to remove previous version
* git clone https://github.com/18f/cf-hello-worlds.git
* choose one of the exmaples there
* cf login -a api.cloud.gov
* cf push <name>-hello
