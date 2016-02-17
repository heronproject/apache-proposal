# Heron Proposal

## Abstract
Heron is a real-time analytics platform that is fully API-compatible with Apache Storm.

## Proposal

Heron is a realtime analytics platform developed by Twitter. It is built to be backwards compatible with Apache Storm's topology API but with a wide array of architectural improvements including increase performance predictability, improve developer productivity and ease manageability. The research paper detailing Heron is available at: http://dl.acm.org/citation.cfm?id=2742788. We wish to develop a community around Heron to increase contributions and see it thrive in an open forum.

## Background

The architecture for Heron is shown here in Figure 1 and Figure 2. Users employ the Apache Storm API to create and submit topologies to a scheduler. The scheduler runs each topology as a job consisting of several containers. One of the containers runs the topology master, responsible for managing the topology. The remaining containers each run a stream manager responsible for data routing, a metrics manager that collects and reports various metrics and a number of processes called Heron instances which run the user-defined spout/bolt code. These containers are allocated and scheduled by scheduler based on resource availability across the nodes in the cluster. The metadata for the topology, such as physical plan and execution details, are kept in Apache Zookeeper.

<img src="https://cloud.githubusercontent.com/assets/367684/10960657/7197f44e-833a-11e5-99c8-34d97051f5e1.png" width="75%"></img>

Figure 1. Heron Architecture

<img src="https://cloud.githubusercontent.com/assets/367684/10960660/7a0c47ce-833a-11e5-89fb-bf6f489c705d.png" width="75%"></img>

Figure 2. Heron Topology Architecture

## Rationale

Heron is built to be used by anyone.

Furthermore, the rapid growth of Heron community is empowered by open source. We believe the Apache foundation is a great fit as the long-term home for Heron, as it provides an established process for community-driven development and decision making by consensus. This is exactly the model we want for future Heron development.

## Initial Goals

* Move the existing codebase, website, documentation, and mailing lists to Apache-hosted infrastructure
* Integrate with the Apache development process
* Ensure all dependencies are compliant with Apache License version 2.0
* Incremental development and releases per Apache guidelines

## Current Status

Heron is a stable project used in production at Twitter for the last couple of years. The Heron source is currently hosted at github.com, which will seed the Apache git repository.

### Meritocracy

By submitting this incubator proposal, we’re expressing our intent to build a diverse developer community around Heron that will conduct itself according to The Apache Way and use meritocratic means of accepting contributions. Several companies have already expressed interest in Heron, and our goal is to grow the Heron community by encouraging open communication, contributions and participation of all types, and ensuring that contributors are recognized appropriately.

### Community

There is a large need for an performant streaming compute system. By bringing Heron into the Apache ecosystem, we believe that the community will grow even bigger.

### Core Developers

Heron was [initially developed](https://blog.twitter.com/2015/flying-faster-with-twitter-heron) at Twitter.

### Alignment

We believe that having Heron at Apache will help further the growth of the streaming compute community, as it will encourage cooperation within the Apache Storm project.

## Known Risks

### Orphaned Products

The risk of the Heron project being abandoned is minimal. It is used in production at Twitter and many companies are interested in using it in production.

### Inexperience with Open Source

Several of the core contributors to the project are familiar with OSS and Apache specifically. Twitter has already moved many projects to the ASF (e.g., Apache Mesos, Apache Aurora, Apache Parquet). We are also mentored by long time ASF incubator members that can help with any roadblocks.

### Homogenous Developers

Initial committers come from a number of companies. Our intention is increase the diversity of contributing developers and their affiliations, and we'll recognize contributions and contributors as the community grows at Apache. We encouraged by interest in the project thus far.

### Reliance on Salaried Developers

It is expected that Heron development will occur on both salaried time and on volunteer time, after hours. The majority of initial committers are paid by their employers to contribute to this project. However, they are all passionate about the project, and we are confident that the project will continue even if no salaried developers contribute to the project. We are committed to recruiting additional committers including non-salaried developers.

### Relationships with Other Apache Products

As mentioned in the Alignment section, Heron is closely related to Apache Storm and Apache Mesos in a numerous ways. Heron also relies on a number of other Apache projects including Apache Thrift and Apache Zookeeper. We look forward to collaborating with those communities.

### An Excessive Fascination with the Apache Brand

Heron is a growing brand in the streaming compute space and we are long time supporters of the Apache brand. This proposal is not for the purpose of generating publicity though. Rather, the primary benefits to joining Apache are those outlined in the Rationale section.

## Documentation

This proposal exists online as http://wiki.apache.org/incubator/HeronProposal. Basic build and usage instructions are included in the existing github repository, and the source code has thorough documentation.

## Source and Intellectual Property Submission Plan

The Heron codebase is currently hosted on Github: https://github.com/heronproject. During incubation, the codebase will be migrated to Apache infrastructure.

## External Dependencies

```
Project | License
Apache Thrift | APL 2
Google Guava | APL 2
```
@TODO

## Cryptography

We do not expect Heron to be a controlled export item due to the use of encryption.

## Required Resources

### Mailing lists

private@heron.incubator.apache.org for private PMC discussions
dev@heron.incubator.apache.org
commits@heron.incubator.apache.org

## Subversion Directory

Git is the preferred source control system: git://git.apache.org/heron

## Issue Tracking

JIRA: Heron (HERON)

## Initial Committers

* Karthik Ramasamy (@TODO: add emails)
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

* Jake Farrell (jfarrell at apache dot org)

### Nominated Mentors

* Jake Farrell (jfarrell at apache dot org)
* Jacques Nadeau (jacques at apache dot org)
* Dave Lester (dlester at apache dot org)
* Julien Le Dem (julien at apache dot org)
* @TODO

### Sponsoring Entity

The Apache Incubator
