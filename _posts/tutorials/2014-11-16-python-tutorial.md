---
layout: article
title:  "Python Read and Write"
categories: tutorials
modified: 2014-11-04T01:01:01
tags: [howto]
toc: true
image:
 teaser: python-logo@2x.png 
share: false
comments: false
ads: false
---


This tutorial is very simple we start two sripts mimicing two devices
talking to each other one acting as a device with two values a PIR
motion sensor and a RELAY that can toggle "true" "false".
<figure>
	<a href="../images/Script_to_script.png"><img src="../images/Script_to_script.png"></a>
	<figcaption>Two scripts talking</figcaption>
</figure>

# Preparations
you need an environment that can run python scripts. 

## Two friending JID's
Setup two accounts on your favourite XMPP site for example
jabber.se. Use any jabber client to test the accounts and make sure
they are friends.

## Get the python code

Clone the code from github. Soon released through SleekXMPP

{% highlight bash session %}
>$ git clone -b xep_0323_325 https://github.com/joachimlindborg/SleekXMPP.git 
{% endhighlight %}


## start the server device

go down to the IoT example catalog. And start one script

{% highlight bash session %}
>$ cd SleekXMPP/examples/IoT
>$ python IoT_TestDevice.py -j yourthing@jabber.se -p passwd -n test
INFO     Negotiating TLS
INFO     Using SSL version: 3
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate COULD NOT BE VERIFIED.
INFO     JID set to: yourthing@jabber.se/544301500141697366520183
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate expiration COULD NOT BE VERIFIED.
{% endhighlight %}

giving a - - debug flag would give more information

{% highlight bash session %}
>$ python IoT_TestDevice.py -j yourthing@jabber.se -p passwd -n test --debug
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
We now start a script that every 6th seconde reads all values from the first.

{% highlight bash session %}
>$ cd SleekXMPP/examples/IoT
>$ python IoT_TestDevice.py -j anotherthing@jabber.se -p passwd -g
yourthing@jabber.se --delay 6
INFO     Negotiating TLS
INFO     Using SSL version: 3
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate COULD NOT BE VERIFIED.
INFO     JID set to: anotherthing@jabber.se/28
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate
expiration COULD NOT BE VERIFIED.

INFO     IoT SEND 323 REQ <iq to="yourthing@jabber.se/98" from="anotherthing@jabber.se/28" id="2" type="get"><req xmlns="urn:xmpp:iot:sensordata" seqnr="2" momentary="true" /></iq>
INFO     IoT RECIEVE <message to="anotherthing@jabber.se/28" from="yourthing@jabber.se/28" xml:lang="en"><fields xmlns="urn:xmpp:iot:sensordata" seqnr="2" done="true"><node nodeId="test"><timestamp value="2015-02-10T03:26:26"><numeric unit="Count" automaticReadout="true" name="Counter" value="3" momentary="true" /><boolean writable="true" automaticReadout="true" name="relay" value="False" momentary="true" /></timestamp></node></fields></message>
INFO     we got fields from yourthing@jabber.se/28 on node test
INFO     (test Counter 3) Count [momentary,automaticReadout,]
INFO     (test relay False) [writable,momentary,automaticReadout,]

{% endhighlight %}

# Writing a value to a device
keep the two scripts above running and start a third one sending a
value change True on the "Toggle" field every 10th second

{% highlight bash session %}
>$ cd SleekXMPP/examples/IoT
>$ python IoT_TestDevice.py -j anotherthing@jabber.se -p passwd -c
yourthing@jabber.se --field "Toggle" --value "True" --delay 10
INFO     Negotiating TLS
INFO     Using SSL version: 3
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate COULD NOT BE VERIFIED.
INFO     JID set to: anotherthing@jabber.se/28
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate
expiration COULD NOT BE VERIFIED.

INFO     IoT will set Toggle to True on to {u'28': {'status': u'',
'priority': 0, 'show': u''}}
INFO     Control callback from yourthing@jabber.se/98 result OK error None
INFO     IoT will set Toggle to True on to {u'28': {'status': u'',
'priority': 0, 'show': u''}}
INFO     Control callback from yourthing@jabber.se/98 result OK error None

{% endhighlight %}

You now see the value of the relay changing once in a while in script
reading values from the first instance.

# What have you done?

You have now sent standardized calls between to endpoints that can be on
any federated xmpp server on internet there are several
https://xmpp.net/directory.php. Just imagin how devices now can talk
between companies in a defined way.
