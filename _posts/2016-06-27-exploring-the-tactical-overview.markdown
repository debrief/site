---
layout: post
title: Exploring the Tactical Overview
date: 2016-06-27 11:39:09.000000000 +01:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: [debrief-help, releases, customisation-example]
tags: [debrief, debrief-update, new-feature]
meta:
  _edit_last: '1'
  post_views_count: '1206'
  _oembed_5c91340ff3aec73919666b3814146424: <iframe width="669" height="502" src="https://www.youtube.com/embed/n4ZO4DAJsaI?feature=oembed"
    frameborder="0" gesture="media" allowfullscreen></iframe>
  _oembed_time_5c91340ff3aec73919666b3814146424: '1508919836'
author: ianmayo
---
<p>For the last year we've been steadily progressing Debrief's data analysis capabilities (read last year's introduction 
<a href="http://debrief.info/have-your-say-on-a-shiny-new-debrief-capability/">here</a>), adding features in packages focussed on analysts' requirements.</p>
<p>The first major realisation of this is in Debrief's new Tactical Overview display, which will be released later on today.</p>
<p>This posting will give you an overview of the capability.</p>
<h2>Background</h2>
<p>Analytical insight is frequently informed by context - understanding the background behind why events happen.   When trying to understand why some particular outcome happened it's invaluable to have as broad as possible awareness of the underlying data.<br />
For example, when analysing interactions, the point at which sensor contact is gained or lost is frequently the focus of analysis effort.  A major part of this analysis is the investigation of why contact was gained or lost.  In the acoustic domain this could be because of any of the following:</p>
<ul>
  <li>Range</li>
  <li>Change in relative spatial geometry (either participant turning to expose a louder/quieter perspective)</li>
  <li>Change in speed</li>
  <li>Change in machinery status/lineup</li>
</ul>
<p>A lot of this information is known to <strong>Debrief</strong>, but is present in different locations.</p>
<h2>Solution</h2>
<p>The <strong>Tactical Overview</strong> display in<strong> Debrief</strong> has been developed as a way of collating as much of this information as possible into a single, time-synced display.  The <strong>Tactical Overview</strong> is a custom instance of the more generic<strong> Stacked Charts</strong> capability.</p>
<img class="alignnone size-large wp-image-3321" src="{{ absolute_url }}/assets/images/Intro.png" alt="First overview" width="669" height="410"/>
<p>Shown on the right of the above screenshot, the <strong>Tactical Overview</strong> provides at-a-glance comparisons of vessel statuses and their relative relationship.   The Orange marker line is shown at the current plot time, allowing the analyst to view all statuses/relationships at the current time.</p>
<p>The view is opened in a single-click from the new <strong>Show Tactical Overview</strong> button in the Track Tote:</p>
<img class="alignnone size-medium wp-image-3322" src="{{ absolute_url }}/assets/images/new-button.png" alt="Track Tote button" width="300" height="148" />
<p>This then uses the current <strong>Primary</strong> and <strong>Secondary</strong> tracks to produce the plot shown below.  As you can see, the top graph shows the vessel courses, the next one speed, then bearing/relative bearing/ ATB, and lastly the range between the vessels.</p>
<img class="alignnone size-large wp-image-3323" src="{{ absolute_url }}/assets/images/InitialView.png" alt="Tactical Overview as shown" width="669" height="410" />
<p>As the time slider is adjusted, an orange <strong>time now</strong> marker moves along the plot (much like the existing <strong>XY Plot views</strong> in<strong> Debrief</strong>).</p>
<p>As you can see, in this case there Speed chart doesn't reveal very much - since the Speed data for this dataset is artificial.   Let's remove it.</p>
<p>In addition to informing your analysis, these charts are a way of you presenting information/data/analysis.  To allow analysts to focus on the data that is relevant, both for analysis &amp; presentation, lots of effort has been invested in being able to easily edit these charts.</p>
<p>So, if we click on the <strong>Edit</strong> button, the chart will switch to edit mode:</p>
<img class="alignnone size-large wp-image-3324" src="{{ absolute_url }}/assets/images/EditMode.png" alt="EditMode" width="669" height="615" />
<p>Here you can see the a breakdown of how the graphs are constructed.  We're going to remove the second graph.  To do this, just click on the orange "<strong>X</strong>" delete button next to <strong>Speed &amp; Depth</strong>. The graph will disappear. Now click on <strong>View</strong> button to return to the view mode.  This will give the first screenshot shown above.</p>
<p>Hold on, let's not skim over the glamorous rotation transition between the two modes.  Here's another look:</p>
<iframe width="669" height="502" src="https://www.youtube.com/embed/n4ZO4DAJsaI?feature=oembed" frameborder="0" gesture="media" allowfullscreen></iframe>
<h2>Advanced usage</h2>
<p>Let's make another change.  Let's imagine that we wish to highlight some significant produce of the relationship between the ATB of the secondary track and the Range. Switch to <strong>Edit</strong> mode, and drag the <strong>Bearing </strong>axis on the middle graph to the bottom-right of the bottom graph - the <em>landing pad</em> titled <strong>Max Axis</strong>.</p>
<p>Ok, now switch back to the <strong>View</strong> mode:</p>
<p>
<img class="alignnone size-large wp-image-3326" src="{{ site.baseurl }}/assets/images/AtbMoved.png" alt="AtbMoved" width="669" height="383" />
</p>
<p>We've now plotted <strong>ATB</strong> against <strong>Range</strong> in the bottom graph.</p>
<p>It's worth exploring the <strong>Edit</strong> view a little more.  Here are some highlights:</p>
<p><img class="alignnone size-large wp-image-3327" src="{{ site.baseurl }}/assets/images/EditView.png" alt="EditView" width="669" height="429" /></p>
<ol>
<li>click here and you can make high level edits to the set of charts. Currently this is covers the horizontal/vertical arrangement of the graphs</li>
<li>click on <strong>Course</strong> to select the top chart, or on the <strong>X</strong> to delete the chart (as you did earlier)</li>
<li>the charts all share a common time axis. Click here to edit the axis, including reversing the direction</li>
<li>lastly, click on the <strong>paintbrush</strong> icon to make formatting changes</li>
</ol>
<p>Note in the following screenshot how the graphs are stacked horizontally and the direction of the time axis has been reversed, to give a traditional waterfall display.</p>
<p><img class="alignnone size-full wp-image-3328" src="{{ site.baseurl }}/assets/images/Waterfall.png" alt="Waterfall" width="574" height="825" /></p>
<p>Another feature of the edit mode is how it is used to add more data.  When in edit mode, if you drag a Debrief track from the Outline view onto either an existing Axis, or the Min Axis / Max Axis placeholder, a dialog will popup asking you which measurement to plot (course, speed, depth):</p>
<p><img class="alignnone size-medium wp-image-3332" src="{{ site.baseurl }}/assets/images/NewMeasurement.png" alt="NewMeasurement" width="300" height="268" /></p>
<p>Tick the box(es) for the data you want, and it will be added to that axis.</p>
<h2>What's next?</h2>
<p>This is an early release, aimed at getting early analyst feedback.</p>
<p>We still have to implement persistence (so that effort invested in customising a set of stacked charts can be saved).  There are also quite a few formatting/layout fixes in the <strong>Edit</strong> view,  more work on how Debrief data is loaded into the view (to view something other than the pre-configured Tactical Overview).</p>
<p>As we add more <a href="http://limpet.info">Limpet</a>-style data analysis capabilities in Debrief, users will be able to view/present more types of data in the stacked charts.</p>
<p>Any feedback on the Tactical Overview is most welcome, either direct to the <a href="mailto:support@Debrief.info">Debrief project</a> or via the GitHub <a href="https://github.com/debrief/debrief/issues">issue repository</a> using the guidance found in <a href="http://debrief.info/how-to-create-a-debrief-issue/">How to Create a Debrief issue</a>.</p>
