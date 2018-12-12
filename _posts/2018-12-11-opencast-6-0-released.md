---
title: Opencast 6.0 has been released
date: 2018-12-11
description: This new major release includes several new features and improvements.
category: release
tags: [release]
---

# Opencast 6: Release Notes

## New Features

- __Asset Manager Storage Layers__ - The Asset Manager now supports multiple storage layers natively. This allows users to move data from local storage to remote storage within Opencast. These moves can be triggered manually, or via a built-in timer. Currently we support local file storage, and AWS S3 storage.
- __Video Editor - Thumbnails__ - When displaying lists of videos, thumbnails are usually used to make such lists more appealing. The video editor allows the user to choose between the default thumbnail (automatically created), a snapshot thumbnail (extract at current position from video stream) or an uploaded thumbnail. This allows the user to get the best thumbnails for his videos with as little effort as possible.
- __Video Editor - Track selection__ - In case multiple tracks have been ingested, the video editor allows the user to choose which tracks should be processed. In case of a dual track lecture recording, the presenter track could be exluded from publication in case the recorded person would want this.
- __Keyboard Shortcuts__ - A per page keyboard shortcut list is available so that users can at any time and page see what keyboard shortcuts are currenlty available.
- __External API 1.1.0__ - For the first time, Opencast takes advantage of its state-of-the-art versioned API by introducing the External API 1.1.0. The new version extends the API to support scheduling of events and access to workflows. The filter and sort facilities have been extended and additional fields are directly delivered by some core requests with allows clients to access them way faster. The External API 1.0.0 is still supported relieving existing clients from the need to be timely adapted.
- __Processing Settings Persistency__ - A new persistence layer for processing settings has been introduced. This allows the Admin UI to not just provide processing settings as input when starting workflows, but also to display processing settings on event basis.
- __Capture Agent Access Management__ - The Admin UI now supports access management for capture agents. This features addresses the need to allow unprivileged users to access the Admin UI to manage their own content and cut videos without allowing them to schedule events or change the scheduling as this task is usually in the responsibility of a dedicated team. It is also possible to permit users access to specific subsets of the available capture agents.
- __New Workflow Operation Handler__
  - __demux__ can be used to demux multiple streams from a container into seperate containers
  - __image-convert__ can convert multiple source images into multiple target images with different encoding
  - __mattermost-notify__ sends notification to services like Mattermost or Slack
  - __move-to-remote__ moves files in the asset manager from one storage system to another
  - __multi-encode__ allows encoding of multiple source tracks into multiple target tracks with differnet encoding
  - __process-smil__ edits media files based on descriptions from a SMIL file
  - __select-tracks__ can filter source tracks based on workflow properties
  - __start-workflow__ allows a workflow to start another workflow

## Improvements

A non-comprehensive list of improvements:

- The event counters are now fully configurable
- Workflows can be stopped and deleted in the Admin UI
- Multiple scheduled events can be edited at once
- Deleting Series now warns if series contains events. You can configure if the user is allowed to delete a series containing events in the series endpoint config file.
- The video editor can be opened while an event is processed
- Add Moodle groups to Moodle role provider
- The order of appearance of workflows can be configured
- Ability to send HTML emails
- Ability for blacklisting languages from the admin UI
- Update LTI Series Tool
- Pre-fill creator metadata field with actual user when creating a new event
- Video editor improvements
- Intuitive Merging of Video Segments
- Add new modal to edit multiple scheduled events at once
- Add ability to hide read-only series and events for unprivileged users
- Lossless Concat Operation
- Update Paella Player to 6.0.x

## Configuration changes
- The tracking options defaults have changed to be more aware of the European Union's General Data Protection Regulation. Note that this is still configurable.
- The role ROLE_UI_EVENTS_DETAILS_GENERAL_VIEW for viewing the publications (previously general) tab in the event details modal has been renamed to ROLE_UI_EVENTS_DETAILS_PUBLICATIONS_VIEW for consistency.
- The introduction of capture agent access management implies that unprivileged users do not have access to any capture agents by default. To allow otherwise unprivileged users to interact with event scheduling, you need to configure their access permissions appropriately. For more details, take a look at the capture agent access management documentation.
