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
</p>
<p>This new capability is intended to enable Debrief Power Users to take on more advanced data manipulation tasks,
including:
<ul>
  <li>Apply bulk changes to Debrief objects</li>
  <li>Import unexpected data-types from file</li>
  <li>Conduct ad-hoc calculations on Debrief data</li>
</ul>
