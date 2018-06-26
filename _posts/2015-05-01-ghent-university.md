---
title: Ghent University
date: 2015-05-01
description: Ghent University is a top 100 university and one of the major universities in Belgium counting over 41,000 students and 9,000 employees. Our 11 faculties offer a wide range of courses and conduct in-depth research in both exact and social sciences.
category: user
tags: [user]
logo: /assets/img/logo-ugent.png
---

## Project Goals
 

Provide an easy to use, flexible and cost effective lecture capture solution to our teachers. Prior to this project no lecture capture solution was available and individual efforts with video recordings were made available on a central streaming server ( Darwin streaming server ).

In order to accommodate students that couldn’t attend lectures a solution was found in Opencast to provide lecture recordings. The project started in 2012 and gradually grew to our current scale. In addition to our initial goal to provide lecture capture for absent students we found out that the project was equally useful as study material for all students and proved a valuable tool to create short knowledge clips in addition to full lecture captures.

## Why Opencast?

### Scalability
A lecture capture solution that is reasonably easy to scale without major financial implications. We can scale up our processing power on short notice, without system downtime.

### Flexibility
The ability to do fully automated lecture capture in addition to manual captures.

### Openness
Open Source software and open design make integrations and alternatives as galicaster and paella player easy to integrate.

## System Overview

### Infrastructure
We run a distributed opencast installation with 7 VM’s, excluding the database servers. All our VM’s run Debian and we use Percona Mysql for a database server.

- 1 Admin server, 2 cores – 24G RAM
- 1 Engage server, 2 cores – 12G RAM
- 2 Worker servers, 8 cores – 8G RAM
- 2 Ingest-Distribution servers, 4 cores – 4G RAM
- 1 Download server, 4 cores – 8G RAM ( Apache static file server )

In addition we have 3 SOLR database servers for the search, series and workflow index and centralized storage via NFS.

Monitoring of the system is managed via zabbix for incidents, grafana for metrics, kibana for log retention and extra metrics and piwik for user statistics.

### Capture agents
We build our own galicaster and galicaster pro capture agents based on Dell Optiplex desktop PC’s. We use datapath capture cards in all our installations.

- 28 Lecture halls equipped with galicaster capture agent
- 6 Mobile capture agents
<img src="http://www.opencast.org/wp-content/uploads/2016/04/IMG1-225x300.jpg">

### Integrations
Our Opencast installation is integrated with our LMS system so that students can view lectures directly in the LMS. We are using the Paella engage player for viewing all lectures.

The integration is currently limited to viewing lectures but we are planning further integration to enable scheduling and managing of lectures within the LMS.

### Usage
We are seeing a steady increase of general usage each semester. The number of unique viewers, lectures viewed and lectures captured increase each semester with an increase before exams and decrease after exams and during the holidays.

<img src="http://www.opencast.org/wp-content/uploads/2016/04/Opencast-Viewer-statistics.png">

### Contact
You can find more detailed information on https://icto.ugent.be/en/content/team-multimedia .

