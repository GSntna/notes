# Azure

## Index


## Fundamentals

### Cloud models

#### Public

* Also known as *multi-tenant*
* Accessible over the internet to everyone
* Everything is owned, configured and set by the cloud provider
* **Advantage**: Easier to use
* **Disavtange**: Security and control of infrastructure

#### Private

* Also known as *single-tenant*
* On-premise or by cloud provider but only accessible through private network
* **Advantage**: Security and privacy
* **Disadvantage**: Cost if hosted on-premise, security if hosted by third-party

#### Hybrid

* Combination between public and private
* Some services are hosted in on-premise or private clouds while some other
services are hosted in a public one. Example: data (private) and application
(public)
* Allows to take the best of both worlds (security, consumption-based, etc.)

### Benefits of cloud computing

#### Availability

Cloud providers offer a *service level agreement (SLA)* that guarantees a
certain level % of availability.

Most common issues for availability:

* **network outage**: applications might need network connectivity to run.
* **application failure**: failiure from bug or application design. Cloud
providers have diagnose software and testing environments to reduce the chance
of application failiure.
* **system outage**: computer running a particular program (db, vm, application)
becomes unavailable. Cloud providers monitor VMs and have systems to recover
unhealthy ones.
* **power outage**: electricity. Cloud providers have battery-operated backups
and *redundant* systems.
* **problem with a reliant system**: relying on external db, apps, or VMs.

#### Scalability

Scaling is the process of adding additional resources or additional power for
an application when needed. There are two variations:

1. horizontal (scaling out): Add more VMs to the application, identical to the
pre-existing. More resources to handle additional load.
2. vertical (scaling up): Move to a new VM with additional resources. More
powerful CPU, more memory, different storing type (ssd) etc.

NOTE: *Scaling in* and *scaling down* can also be used when less resources are
needed to save costs.

#### Elasticity

The ease of scaling in both directions. Cloud providers can automatically
scale depending on the usage patter of the applicaiotn.

#### Reliability and predictability

Unhealthy systems might go wrong. Cloud providers monitor the health of cloud
resources and take action when necessary, ensuring the cloud is *fault tolerant*.

It also ensures that the data is safe when theres a natural disaster where the
servers are hosted. Disaster recovery plans are referred as *Business*
*Continuity and Disaster Recovery (BCDR)*.

#### Security and governance

Cloud providers monitor networks and systems used by the cloud and when threats
are identified they are eliminated. Security is taken care of by the Clould
provider.

Governance is also easy, defining who can acces the resources and defining level
of access.

#### Manageability in the cloud

Cloud providers have tools to make the handling of the cloud services easier to
the end user.

### Cloud services types
