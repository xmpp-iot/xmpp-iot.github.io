---
layout: article
title:  "Python tutorial Read and Write"
categories: tutorials
modified: 2014-11-04T01:01:01
tags: [howto]
toc: true
image:
	feature: 400x250.gif 
share: false
comments: false
ads: false
---


This tutorial is very simple it just starts up a device and then uses another script to control it.
# Preparations
you need an environment that can run python scripts. 

## Two JID's
first setup two accounts on your favourite XMPP site for example jabber.se

## Get the python code

Clone the code from github

{% highlight bash session %}
Joachims-MacBook-Pro:IoT joachimlindborg$ git clone -b xep_0323_325 https://github.com/joachimlindborg/SleekXMPP.git 
{% endhighlight %}


## start the server device

{% highlight bash session %}
Joachims-MacBook-Pro:IoT joachimlindborg$ python IoT_TestDevice.py -j yourthing@jabber.se -p passwd -n test 
INFO     Negotiating TLS
INFO     Using SSL version: 3
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate COULD NOT BE VERIFIED.
INFO     JID set to: yourthing@jabber.se/544301500141697366520183
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate expiration COULD NOT BE VERIFIED.
{% endhighlight %}

giving a debug flag would give more information

{% highlight bash session %}
Joachims-MacBook-Pro:IoT joachimlindborg$ python IoT_TestDevice.py -j yourthing@jabber.se -p passwd -n test --debug
DEBUG    Loaded Plugin: RFC 6120: Stream Feature: STARTTLS
DEBUG    Loaded Plugin: RFC 6120: Stream Feature: Resource Binding
DEBUG    Loaded Plugin: RFC 3920: Stream Feature: Start Session
DEBUG    Loaded Plugin: RFC 6121: Stream Feature: Roster Versioning
DEBUG    Loaded Plugin: RFC 6121: Stream Feature: Subscription Pre-Approval
DEBUG    Loaded Plugin: RFC 6120: Stream Feature: SASL
DEBUG    Loaded Plugin: XEP-0030: Service Discovery
DEBUG    Loaded Plugin: XEP-0323 Internet of Things - Sensor Data
DEBUG    Loaded Plugin: XEP-0325 Internet of Things - Control
DEBUG    Loaded Plugin: XEP-0199: XMPP Ping
DEBUG    Device object started nodeId test
DEBUG    fields{'Counter': {'dataType': None, 'type': 'numeric', 'unit': 'Count'}, 'Relay': {'dataType': None, 'type': 'numeric', 'unit': 'Bool'}}
DEBUG    momentary{}
DEBUG    momentary updated{'Counter': {'flags': {'momentary': 'true', 'automaticReadout': 'true'}, 'value': '0'}}
DEBUG    fields{'Counter': {'dataType': None, 'type': 'numeric', 'unit': 'Count'}, 'Relay': {'dataType': None, 'type': 'numeric', 'unit': 'Bool'}}
DEBUG    momentary{'Counter': {'flags': {'momentary': 'true', 'automaticReadout': 'true'}, 'value': '0'}}
DEBUG    momentary updated{'Counter': {'flags': {'momentary': 'true', 'automaticReadout': 'true'}, 'value': '0'}, 'Relay': {'flags': {'writable': 'true', 'momentary': 'true', 'automaticReadout': 'true'}, 'value': '0'}}

{% endhighlight %}


# Reading a value from a device
We now start a script that continiously reads values from the first.

# Writing a value to a device
keep the two scripts above running ans start a third one changing values in the sever device. 
