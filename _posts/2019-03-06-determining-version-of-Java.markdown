---
layout: post
title: 'Determining version of Java'
date: 2019-03-06 09:52:08.000000000 +00:00
categories: [debrief-help]
meta:
  post_views_count: '04'
author: ianmayo
---
<p>On occasion it's useful to determine the version of Java that a Debrief installation is using.</p>
<p>Follow this process to determine the version:
<ol>
  <li>Open Debrief</li>
  <li>Click on `Help` / `About Debrief NG`</li>
  <li>From the dialog that opens, click on `Installation details`</li>
  <li>The `DebriefNG installation details` dialog will open</li>
  <li>Open the `Configuration` tab</li>
  <li>Scroll down to the `-arch` entry.  If this ends in `_64` then it's a 64-bit java installation, otherwise it's 32-bit.</li>
</ol>
<img class="img-fluid" src="{{ site.baseurl }}/assets/images/JVM_Version_Screenshot.png" alt="Viewing JVM Version" />
</p>
