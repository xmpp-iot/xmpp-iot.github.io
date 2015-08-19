---
layout: archive
title: "Gsoc 2015"
date: 2015-03-001T09:44:20-04:00
modified:
categories: 
excerpt: "XMPP-IoT is part of Google summer of code 2015"
image:
  feature: 
  teaser: prototyping-iot_400x250.png
  thumb: prototyping-iot_400x250.png
share: true
ads: false
---
***Prototyping tools for IoT*** is a project that is part of the [google summer of code 2015](http://www.google-melange.com/gsoc/homepage/google/gsoc2015). The project will blog here about proceedings and the evolvement.
Deliverables
* IoT Prtocols implementation for XMPP Chat Client Converse.Js
* Cross Platform Mobile Application for Sensoring and Controlling of Data sent or received by Devices
* History Logger for Sensor Devices
<div>
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
<script type="text/javascript" src="js/storyjs-embed.js"></script>
<script>
	$(document).ready(function() {
	createStoryJS({
		type:		'timeline',
		width:		'600',
		height:		'200',
		source:		'data.json',
		embed_id:	'my-timeline',
		debug:		true
		});
	});
</script>
</div>
<div class="tiles">
{% for post in site.categories.gsoc %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
