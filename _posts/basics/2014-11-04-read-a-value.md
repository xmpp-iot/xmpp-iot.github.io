---
layout: article
title:  "Readout from a device"
categories: basics
modified: 2014-11-04T02:02:02
tags: [basics]
toc: true
comments: false
share: false
ads: false
---

The first you would like to do in an Internet of Things environment is to read values from your Thing. The device can of course have several available values here we show a simple readout getting all available values that you as a peer has access to. More details on the read process is in the [xmpp specification](http://xmpp.org/extensions/xep-0323.html)

##Read all fields available

Readout of all momentary fields from a Thing (device) 

**Request to another peer**
{% highlight xml %}
<iq type='get'
  from='client@clayster.com/amr'
  to='device@clayster.com'
  id='S0001'>
  <req xmlns='urn:xmpp:iot:sensordata' seqnr='1' momentary='true'/>
</iq>
{% endhighlight %}

**The respons confirming the readout**
{% highlight xml %}
<iq type='result'
  from='device@clayster.com'
  to='client@clayster.com/amr'
  id='S0001'>
  <accepted xmlns='urn:xmpp:iot:sensordata' seqnr='1'/>
</iq>
{% endhighlight %}

**next respons with the data contained**
{% highlight xml %}
<message from='device@clayster.com'
  to='client@clayster.com/amr'>
  <fields xmlns='urn:xmpp:iot:sensordata' seqnr='1' done='true'>
    <node nodeId='Device01'>
      <timestamp value='2013-03-07T16:24:30'>
        <numeric name='Temperature' momentary='true' automaticReadout='true' value='23.4' unit='°C'/>
        <numeric name='load level' momentary='true' automaticReadout='true' value='75' unit='%'/> 
      </timestamp>
    </node>
  </fields>
</message>
{% endhighlight %}

*Observe the "done='true'" above meaning that this was a single respons


##Read all fields inside a node in the device
Devices can have different subparts called nodes. You can ask a specific node for all it' fields.

##Read a specific field inside a node in the device
Of course you can readout a specific field within a specific node inside the device.

##Parent restricting the access
For every request the device should ask it's parent the trusted party if the request is allowed the trusted party can reject the request and the device can cache that information for later use.


`Parent:` A parent is an optional peer being the device Best friend or trusted party and is responsible for providing the device with the access priviliges for different peers.
{: .notice-inverse}
`Node:` A Thing can model it's content in several "nodes" for example a heatpump can model it's content as the nodes *Pump*, *WaterHeater*, *Compressor* which all can have several fields. 
{: .notice-inverse}
`Field:` A Thing can have several **fields** every field is a low level value having some type of SI unit such as kWh, temp in F,C or K. 
{: .notice-inverse}


[pidgin-ex]: http://im.about.com/od/imfornewusers/ss/pidgin-account-adding-contacts.htm

