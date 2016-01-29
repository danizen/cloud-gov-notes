# CloudNative DevOps with Cloud.gov Notes

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

* Create an account - you should receive an invitation to a Sandbox account, but can try at other CloudFoundry implementations.
* Download cf cli from releases area of https://github.com/cloudfoundry/cli and note also https://docs.cloudfoundry.org/devguide/installcf/install-go-cli.html to remove previous version
* `git clone https://github.com/18f/cf-hello-worlds.git`
* choose one of the exmaples there
* `cf login -a api.cloud.gov`
* `cf push <name>-hello`

Questions:

* _Does it run tests?_
  - No - cloud.gov handles the continuous deployment part.   https://docs.cloud.gov/apps/continuous-deployment/ provides details on integration with various CI servers.
* _Do I have to use github?_   
  - No.
* _Is there a Java hello world?_
  - Previously answered as coming soon.
* _Can I get the code from a running app?_
  - The official answer is no.   There's a hacky way to do it.
* _So, buildpacks run in warden containers managed by the droplet execution agents?_
  - There's a separate component that does the management, but yes, warden containers which include the result of combining the buildpack with the application code are run on droplet execution agents (DEAs).
* _Does CloudFoundry use Docker_?
  - CloudFoundry does support Docker images within it, but cloud.gov does not as yet.
