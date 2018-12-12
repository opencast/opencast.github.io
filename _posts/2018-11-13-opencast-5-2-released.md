---
title: Opencast 5.2 has been released
date: 2018-11-13
description: Please note that this maintainance release contains a breaking configuration change!
tags: [release, paella, player, animate, live, scheduler, OAI-PMH, moodle]
---

Please note that this maintainance release contains a breaking configuration change. More information can be found in admin [upgrade guide](https://docs.opencast.org/r/5.x/admin/upgrade/#configuration-changes-since-opencast-52) or on the [mailing list](https://groups.google.com/a/opencast.org/forum/#!topic/users/LehzK55BIfU).


### Opencast 5.2

*Released on November 13, 2018*

- [[MH-13144](https://opencast.jira.com/browse/MH-13144)][[#553](https://github.com/opencast/opencast/pull/553)] -
  only set Job startDate if no set before
- [[MH-13216](https://opencast.jira.com/browse/MH-13216)][[#550](https://github.com/opencast/opencast/pull/550)] -
  Fix Documentation Pages
- [[MH-13211](https://opencast.jira.com/browse/MH-13211)][[#547](https://github.com/opencast/opencast/pull/547)] -
  engage-ui: Fix live schedule bug: event available before schedule
- [[MH-13190](https://opencast.jira.com/browse/MH-13190)][[#520](https://github.com/opencast/opencast/pull/520)] -
  Factor out JpaGroupRoleProvider JaxRs REST to mitigate load cycle race
- [[MH-13189](https://opencast.jira.com/browse/MH-13189)][[#517](https://github.com/opencast/opencast/pull/517)] -
  Fix paella xss security isues in opencast 5.x
- [[MH-13167](https://opencast.jira.com/browse/MH-13167)][[#490](https://github.com/opencast/opencast/pull/490)] -
  Republishing metadata does not update all metadata
- [[MH-13152](https://opencast.jira.com/browse/MH-13152)][[#476](https://github.com/opencast/opencast/pull/476)] -
  Reduce Workflow Messages
- [[MH-13138](https://opencast.jira.com/browse/MH-13138)][[#463](https://github.com/opencast/opencast/pull/463)] -
  Fix media module language configuration
- [[MH-13108](https://opencast.jira.com/browse/MH-13108)][[#437](https://github.com/opencast/opencast/pull/437)] -
  Prevent permission problem in Travis cache
- [[MH-13091](https://opencast.jira.com/browse/MH-13091)][[#421](https://github.com/opencast/opencast/pull/421)] -
  Concat operation problem with FFMPEG 4.x
- [[MH-13069](https://opencast.jira.com/browse/MH-13069)][[#406](https://github.com/opencast/opencast/pull/406)] -
  Update problematic admin interface libraries
- [[MH-12976](https://opencast.jira.com/browse/MH-12976)][[#389](https://github.com/opencast/opencast/pull/389)] -
  custom role patterns not working
- [[MH-12387](https://opencast.jira.com/browse/MH-12387)][[#350](https://github.com/opencast/opencast/pull/350)] -
  Fix CAS

The Opencast codebase is now located on [GitHub](https://github.com/opencast/opencast).

A full list of changes can be found in the [official release notes](https://docs.opencast.org/r/5.x/admin/releasenotes/).

Visit the [installation guide](https://docs.opencast.org/r/5.x/admin/installation/) for more information on how to get Opencast 5.
