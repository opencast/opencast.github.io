---
title: Opencast Annotation Tool 2.0 - QA started
date: 2018-07-30
description: For the upcoming release 2.0 of the Annotation Tool we need help for the QA  
category: news
tags: [annotation-tool, qa, testing]
image: assets/img/AnnotationTool2-0.jpg
---

The [Opencast Annotation Tool](https://github.com/opencast/annotation-tool) is an enhancement for Opencast to annotate videos in a scientific way. Within the last months the [ELAN e.V.](https://www.elan-ev.de/) was able to continuously improve the tool, thanks to the sponsoring of the [University of Muenster](https://www.uni-muenster.de/studium/orga/electures.html) (Germany).

[<img class="center-image" src="assets/img/AnnotationTool2-0.jpg">](https://github.com/opencast/annotation-tool)

Now we feel the time has come to create an new release that includes all the new features that we have added so far. This release should be so stable and reliable that current Opencast adopter could use it without any concerns. That is why we need your help! Only if this release is tested carefully, we can ensure its quality.

For those of you not running an Opencast test server on your own, we setup a testing instance:

[https://interactivevideo.virtuos.uos.de/](https://interactivevideo.virtuos.uos.de/)

```
User: admin
Password: opencast
```

Feel free to add additional users and upload your own video. If you encounter any technical problems using this system, please contact [Julian](mailto:kniephoff@elan-ev.de) or [Rüdiger](mailto:rrolf@uni-osnabrueck.de).

When uploading a video you should regard two things:

1. When selecting the workflows, make sure "Opencast Annotation Tool" is checked as a distribution channel.
2. When setting the access policy for the event, make sure that at least the same rights are set like in the template "annotate". You might even add additional rules, where you give a certain user "annotate-admin" rights, i.e.

After the event is processed the list of publications the "Annotation Tool" should show up.

If you encounter an error, please file an issue in Github:

[https://github.com/opencast/annotation-tool/issues](https://github.com/opencast/annotation-tool/issues)

For each ticket please select the milestone "Annotation Tool 2.0".

If you find an error that prevents you from continuing testing please set the label *"blocker"*. If you find a severe problem that needs to be fixed for the release please select the label *"critical"*.

We would also recommend to use the labels *"usability"*, *"accessibility"* and *"documentation"*, if appropriate, for a better organization of  the tickets.

If you find issues that you suspect to fail in Opencast and not in the annotation tool, please report them in the [Opencast Jira](https://opencast.jira.com/).


If you are running an own Opencast test instance, feel free to checkout this release candidate:

[https://github.com/opencast/annotation-tool/tree/r/2.x](https://github.com/opencast/annotation-tool/tree/r/2.x)

Thank you for your support to improve the Annotation Tool!
