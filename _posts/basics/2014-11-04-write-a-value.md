---
layout: article
title:  "Write a value to a device"
categories: basics
modified: 2014-11-04T02:02:02
tags: [basics]
toc: true
comments: false
share: false
ads: false
image:
	feature: 400x250.gif
---

The next you would like to do in an Internet of Things environment is
to write values to your Thing. The device can of course have several
available fields that can be written. Here we show a simple write of a
value to one field that you as a peer has access to. More details on the write process is in the [xmpp specification](http://xmpp.org/extensions/xep-0325.html)

##Write a value to a field

Write tha value true to the field relay on a Thing (device) 

**Request to another peer**
{% highlight xml %}
<iq type='set'
  from='client@clayster.com/amr'
  to='device@clayster.com'
  id='S0001'>
  <req xmlns='urn:xmpp:iot:sensordata' seqnr='1' momentary='true'/>
</iq>
{% endhighlight %}

**The respons confirming the write**
{% highlight xml %}
<iq type='result'
  from='device@clayster.com'
  to='client@clayster.com/amr'
  id='S0001'>
  <accepted xmlns='urn:xmpp:iot:sensordata' seqnr='1'/>
</iq>
{% endhighlight %}


##Writing to several fields


##Parent restricting the access
For every request the device should ask it's parent the trusted party if the request is allowed the trusted party can reject the request and the device can cache that information for later use.


`Parent:` A parent is an optional peer being the device Best friend or trusted party and is responsible for providing the device with the access priviliges for different peers.
{: .notice-inverse}
`Node:` A Thing can model it's content in several "nodes" for example a heatpump can model it's content as the nodes *Pump*, *WaterHeater*, *Compressor* which all can have several fields. 
{: .notice-inverse}
`Field:` A Thing can have several **fields** every field is a low level value having some type of SI unit such as kWh, temp in F,C or K. 
{: .notice-inverse}



