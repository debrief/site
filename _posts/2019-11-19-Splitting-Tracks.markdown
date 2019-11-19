---
layout: post
title: 'New Feature: Splitting Tracks'
date: 2019-11-19 09:52:08.000000000 +00:00
image: '/assets/images/SplitTracksMenu_Clipped.png'
categories: [debrief-help]
meta:
  post_views_count: '02'
author: ianmayo
---

Learn more about handling periods of missing data in Debrief

# Missing data

By default, Debrief joins all track points with straight lines.

But, when there is a period of missing data, the viewer of a report may
mistakenly think the platform is on steady course and speed.

In circumnstances such as these, it would make more sense to split a track into several segments (legs).

A split in the track can be recognised by a period of missing data. Depending on the frequency of the data, a gap may be represented by one minute or one hour of missing data.

Here is an example of a track with missing periods of data.

<img class="img-fluid" src="{{ site.baseurl }}/assets/images/TrackWithJumps.png" alt="Tracks with jumps" />

By splitting the track into segments, we can convey the periods of missing data.

# Right-click menu

We've added a new right-click menu option for tracks.  On selecting `Split track into segments...` a drop-down menu of time interval sizes is offered:
<img class="img-fluid" src="{{ site.baseurl }}/assets/images/SplitTracksMenu.png" alt="split tracks menu" />

Once clicked, any selected tracks are inspected, being split into segments whenever there is a period of missing data greater than the provided threshold.

Here's a split track.

<img class="img-fluid" src="{{ site.baseurl }}/assets/images/SplitTrack.png" alt="split tracks" />

# Formatting helper

Right-clicking on a track is fine for individual tracks, but if you're processing a high volume of tracks, you may wish to auto-split them on missing data.

Learn more about them here: [ https://debrief.github.io/tutorial/reference.html#replay_format_annotations](https://debrief.github.io/tutorial/reference.html#replay_format_annotations)

This can be supported by inserting `Formatting Helper` instructions into a `.rep` file.  These are commands that advice Debrief on how to process data loaded from that file.

See the instruction below:

````
;SPLIT_TRACK: One_Hour 3600000 PLATFORM_HOST
````

This instructs Debrief to look out for any track called `PLATFORM_HOST`, and split it whenever there is a gap of 3.6 million milliseconds (that's one hour in new money).

````
;SPLIT_TRACK: 48_Hours 172800000 
````

This instructs Debrief to split any track when there is a gap of more than 48 hours from the previous measured position.

