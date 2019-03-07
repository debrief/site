---
layout: post
title: 'Determining version of Java'
date: 2019-03-06 09:52:08.000000000 +00:00
categories: [debrief-help]
meta:
  post_views_count: '04'
author: ianmayo
---

On occasion it's useful to determine the version of Java that a Debrief installation is using.

Follow this process to determine the version:

  1. Open Debrief
  2. Click on `Help` / `About Debrief NG`
  3. From the dialog that opens, click on `Installation details`
  4. The `DebriefNG installation details` dialog will open
  5. Open the `Configuration` tab
  6. Scroll down to the `-arch` entry.  If this ends in `_64` then it's a 64-bit java installation, otherwise it's 32-bit.

<img class="img-fluid" src="{{ site.baseurl }}/assets/images/JVM_Version_Screenshot.png" alt="Viewing JVM Version" />

