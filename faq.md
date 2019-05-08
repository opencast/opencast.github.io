---
title: Frequently Asked Questions
description: Here are some frequently asked questions regarding Opencast. This will help you determine if it’s the right solution for your organization.
---
{% include software_menu.html %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## How much does it cost?

Opencast is free, open source software. There is no direct cost associated with downloading and deploying the software. As open source software, there is free support from the community on the [Opencast mailing lists](communication.md) and the [Opencast IRC channel](communication.md). If you require enterprise-level support, there are [commercial vendors](support.md) that provide that service. Opencast can run both on premises, or in the cloud, whichever works better for you!" %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## How long does it take to setup an Opencast system?

Setting up an Opencast cluster can be done in a few hours, using a single machine. Opencast is typically a building block within a larger video capture ecosystem and it is highly customizable, so a full customization and tuning to your particular needs generally is typically planned for a 1-3 month deployment window depending on the complexity of your project. For Universities, there is often a small pilot rolled-out and tested before a campus-wide solution is developed."%}


{% include simplebox.html backgroundcolor=site.data.colors.box
content="## How well will it integrate with what we already have?

Opencast was developed as an open source solution so that it will work well in any environment. The Opencast Marketplace is full of technology providers with active integrations, but the open API lets you develop any integration that’s needed. Opencast uses the iCalendar, RSS, ATOM, OAI-PMH, MPEG-7, Dublin Core, LTI, and REST standards.  Opencast also integrates with Sakai, and Moodle, using CAS, Shibboleth, or LDAP for user role data.  Other integrations are possible, but likely will require development time." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## How does Opencast compare to proprietary solutions?

Our community feedback emphasizes the extensive flexibility and scalability of the Opencast platform. It has all the common features built-in with the ability to add any features you require without the development cycles of proprietary solution providers.  Opencast also has an open data model: Your data is yours, no fees to get it back, and no proprietary formats." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Will students and professors like it?

Educators love Opencast because once it’s set up, they don’t have to worry about much. Lectures are automatically queued to record, so there is little day-to-day management. Students benefit from the easy access to videos on CMS, iTunes, YouTube or RSS subscriptions. Advanced search features also help end-users find the content they are looking for quickly and easily.  Access to various features can be controlled at a fine grain as well.  For example, faculty who wish to start and stop their own recordings can do so, and can be given the ability to edit the recordings prior to release." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Why is open source the best option?

Open source is a great way to highlight your organization’s drive for innovation by contributing back to the community. Because Opencast is a community-based solution, you have the benefit of learning directly from and collaborating with like-minded organizations. Open source solutions also have a longer ‘shelf-life’ because the active community is continuing to develop and you don’t have to worry about a software provider discontinuing elements of their software or hardware – which can become extremely costly to replace. You can also continue to change and develop software to address your needs, so it allows for much more flexibility, and more seamless integration with your other IT-systems." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## How often are new features rolled out by the community?

Every year there are two major releases of Opencast.  These major releases contain new features, as well as bug fixes.  These releases can be disruptive, and usually require manual upgrades.  Maintenance releases are released on an on-going basis and contain only bug fixes and performance improvements.  These releases can be deployed at any time and should not have a negative impact day-to-day operations." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## How do I get started?

Take a look at our [getting started](getting-started.md) page!" %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## What databases does Opencast support?

We directly support MariaDB, however there are community members using PostgreSQL." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## How does Opencast scale?  Does it support clustering?

Opencast spreads its load over its worker nodes.  If you need more scale, you add more workers.  It's as simple as that.  The user facing components can be clustered, and content can even distributed directly from the cloud." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Does Opencast support virtual portals or multiple organizations?

Yes!  Opencast's allows the same underlying hardware to be referred to by multiple virtual hosts, and share the same underlying resources for processing.  For example, http://a.example.org, and http://b.example.org could both be running on http://hardware.example.org, and yet be unaware of the other organization.  This drastically simplifies life for cloud hosting providers wishing to provide Opencast as a service." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Can I customize Opencast

Yes!  Opencast is easy to skin, although most institutions embed the player into their CMS.  Adding new features and services is also easy, and more importantly __possible__, when compared with proprietary systems." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Can redistribute my changes?  What is your license?

Yes!  Opencast is licensed [ECL2](https://github.com/opencast/opencast/blob/develop/LICENSE), so feel free to distribute your changes.  One suggestion before you do this: If you contribute those changes to the project then *we maintain them*, rather than spending your resources.  This is the power of Open Source." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## What kind of influence can I have in the feature and future direction of Opencast?

Lots!  You can enter feature requests in [JIRA](https://opencast.jira.com), and participate in [community discussions](communication.md) without contributing code.  You can run for election to the Opencast board, which sets non-technical goals and helps administer the community as a whole.  The best way to influence Opencast's direction is code: [File pull requests](https://github.com/opencast/opencast/pulls), and eventually become a committer.  Our committers make the final, technical decisions about which features make a given release.  We operate on a meritocracy style where committer rights are granted to those who we feel have shown enough investment in the community.  Once you are a committer you can vote on technical decisions, commit code, and can help Opencast move forward as a product." %}
{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Are there conferences for Opencast?

Yes!  We host an annual conference in late January or earch February, and typically have a representative at Open Apereo as well.  Watch our homepage for news on our conference, and Apereo's page for news on theirs!  Our conference is the best place for focussed technical talks about Opencast, whether discussing the deep internals, or how a institution can run Opencast at scale in production.  The conference is also the best place for networking, with most if not all of our committers present." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Are there training courses for Opencast?

Yes!  Some of our [commercial providers](support.md) offer training, both for individual institutions, and larger shared venues.  Contact the vendors, or watch on the [mailing lists](communication.md) for more details." %}

{% include simplebox.html backgroundcolor=site.data.colors.box
content="## Does Opencast support mobile devices for playback?

Yes!  [Our player](https://paellaplayer.upv.es/) supports mobile devices." %}

{% include software.html %}

