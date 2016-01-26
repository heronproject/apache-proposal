# Heron Proposal

## Abstract
Heron is a real-time analytics platform that is fully API-compatible with Storm.

See the research paper for more details: http://dl.acm.org/citation.cfm?id=2742788

## Proposal

When developing Heron, our main goals were to increase performance predictability, improve developer productivity and ease manageability.

## Background

The overall architecture for Heron is shown here in Figure 1 and Figure 2. Users employ the Storm API to create and submit topologies to a scheduler. The scheduler runs each topology as a job consisting of several containers. One of the containers runs the topology master, responsible for managing the topology. The remaining containers each run a stream manager responsible for data routing, a metrics manager that collects and reports various metrics and a number of processes called Heron instances which run the user-defined spout/bolt code. These containers are allocated and scheduled by scheduler based on resource availability across the nodes in the cluster. The metadata for the topology, such as physical plan and execution details, are kept in Zookeeper.

<img src="https://cloud.githubusercontent.com/assets/367684/10960657/7197f44e-833a-11e5-99c8-34d97051f5e1.png" width="75%"></img> 

Figure 1. Heron Architecture

<img src="https://cloud.githubusercontent.com/assets/367684/10960660/7a0c47ce-833a-11e5-89fb-bf6f489c705d.png" width="75%"></img> 

Figure 2. Heron Topology Architecture

## Rationale

Heron is built to be used by anyone.

Furthermore, the rapid growth of Heron community is empowered by open source. We believe the Apache foundation is a great fit as the long-term home for Heron, as it provides an established process for community-driven development and decision making by consensus. This is exactly the model we want for future Heron development.

## Initial Goals

* Move the existing codebase to Apache
* Integrate with the Apache development process
* Ensure all dependencies are compliant with Apache License version 2.0
* Incremental development and releases per Apache guidelines

## Current Status

Heron is a stable project used in production at Twitter for the last couple of years. The Heron source is currently hosted at github.com, which will seed the Apache git repository.

### Meritocracy

We plan to invest in supporting a meritocracy. We will discuss the requirements in an open forum. Several companies have already expressed interest in this project, and we intend to invite additional developers to participate. We will encourage and monitor community participation so that privileges can be extended to those that contribute.

### Community

There is a large need for an performant streaming compute system. By bringing Heron into Apache, we believe that the community will grow even bigger.

### Core Developers

Heron was [initially developed](https://blog.twitter.com/2015/flying-faster-with-twitter-heron) at Twitter. 

### Alignment

We believe that having Heron at Apache will help further the growth of the streaming compute community, as it will encourage cooperation within the Storm project. In the long term and when the project graduates from the Apache incubator, we would be amenable to have the project join the Storm project.

## Known Risks

### Orphaned Products

The risk of the Heron project being abandoned is minimal. It is used in production at Twitter and many companies are interested in using it in production.

### Inexperience with Open Source

Several of the core contributors to the project are familiar with OSS and Apache specifically. Twitter has already moved many projects to the ASF (e.g., Parquet and Mesos). We are also mentored by long time ASF incubator members that can help with any roadblocks.

### Homogenous Developers

The initial committers come from a number of companies TODO

### Reliance on Salaried Developers

It is expected that Heron development will occur on both salaried time and on volunteer time, after hours. The majority of initial committers are paid by their employers to contribute to this project. We are committed to recruiting additional committers including non-salaried developers. 

### Relationships with Other Apache Products

As mentioned in the Alignment section, Heron is closely related to Storm and Mesos in a numerous ways. We look forward to collaborating with those communities.

### An Excessive Fascination with the Apache Brand

Heron is a growing brand in the streaming compute space and we are long time supporters of the Apache brand. This proposal is not for the purpose of generating publicity though. Rather, the primary benefits to joining Apache are those outlined in the Rationale section.

## Documentation

Documentation is currently located as README markdown files:

* TODO

## Source and Intellectual Property Submission Plan

The Heron codebase is currently hosted on Github: https://github.com/heronproject. 

This is the exact codebase that we would migrate to the Apache foundation.

## External Dependencies

```
Project | License
Apache Thrift | APL 2
Google Guava | APL 2
TODO
```
More TODO

## Cryptography

We do not expect Heron to be a controlled export item due to the use of encryption.

## Required Resources

### Mailing lists

heron-dev
heron-user

## Subversion Directory

Git is the preferred source control system: git://git.apache.org/heron

## Issue Tracking

JIRA: Heron (HERON)

## Initial Committers

* Karthik Ramasamy 
* Maosong Fu 
* Nikunj Bhagat 
* Sailesh Mittal 
* Vikas Ramesh Kedigehalli
* Siddharth Taneja
* Bill Graham
* Chris Kellogg
* Andrew Jorgensen
* Jingwei Wu

## Affiliations

* Karthik Ramasamy (Twitter)
* Maosong Fu (Twitter)
* Nikunj Bhagat (Google)
* Sailesh Mittal (Twitter)
* Vikas Ramesh Kedigehalli (Twitter)
* Siddharth Taneja (Google)
* Bill Graham (Twitter)
* Chris Kellogg (Twitter)
* Andrew Jorgensen (Twitter)
* Jingwei Wu (Twitter)

## Sponsors

### Champion

* TODO

### Nominated Mentors

* Jacques Nadeau
* Dave Lester
* TODO

### Sponsoring Entity

The Apache Incubator
