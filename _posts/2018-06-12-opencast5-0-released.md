---
title: Opencast 5.0 has been released
date: 2018-06-12
description: This new release includes the popular Paella Player, a new Animate service to create exciting trailers, a Live Streaming Scheduler and many more improvements.
category: release
tags: [release, paella, player, animate, live, scheduler, OAI-PMH, moodle]
---

The new features for this release are:


* **Paella Player** - The Paella Player is already well known in the Opencast community as external plugin, but now the
  player is finally integrated into Opencast's core. This makes switching players as easy as changing one configuration
  property. Additional improvements include more translations as well as caption support.

* **Animate Service** - The animate service can be used to generate custom animated video sequences which can use
  Opencast's metadata like the author's name or the event's title. This is useful, for example, to automatically generate
  animated intro sequences to ensure having a homogeneous corporate design for all video recordings.

* **Live Scheduler Service** - With the live scheduler service you are able to schedule and publish live events. The
  students can then watch the stream while the recording is happening.

* **OAI-PMH Publication Service** - OAI-PMH publication service was created to simplify and unify the publishing process
  to OAI-PMH repositories. The metadata update handling was also improved in speed and robustness.

* **Moodle User/Role Provider** - The Moodle user/role provider allows to query Moodle users and their roles.

* **New Workflow Operation Handlers**
    * **clone** - The clone workflow operation can be used to clone media package elements.
    * **duplicate-event** - The duplicate-event operation can be used to duplicate an event by copying an existing one.
    * **log** - The log workflow operation can be used to log the current state of a workflow for testing and debugging purposes.
    * **animate** - The animate workflow operation handler is the entry point to the new animate service.

* **User Interface Improvements**
    * New translations added: Filipino, Tagalog and Turkish
    * Additional workflow controls have been added to the adminitration user interface.
    You can stop running or delete the previous started workflows.
    * New recordings can be scheduled by specifying the end time or duration.
    * A click on the recording date in the adminitrative interface event overview will set an filter
    for recordings at the same date.
    * Event dialog publications tab has been improved. You can define the name, icon and the order of the publications.
    * Default workflow is preselected in event create dialog.
    * The video editor can optionally play segments that are marked for deletion.
    * The save button in the video editor do not close the editor any more.
    For this purpose you can use the close button that is placed beside.
    * You will see an warning message by leaving the video editor with unsaved changes.

* **Other improvements**
    * Series index and workflow index rebuild performance improved.


The Opencast codebase is now located on [GitHub](https://github.com/opencast/opencast).

A full list of changes can be found in the [official release notes](https://docs.opencast.org/r/5.x/admin/releasenotes/).

Visit the [download section](http://www.opencast.org/software/download) for more information on how to get Opencast 5.0.
