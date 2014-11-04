---
Layout: article
title:  "Read a value from a node"
categories: basics
modified: 2014-11-04
share: false
ads: false
---

The first thing you would like to do in an Internet of Things environment is to read values from a thing. The thing can of course have several available values 

#Read all fields available

Read all momentary fields from a Thing returning all fields that I have access to

{% highlight XML %}
<iq type='get'
       from='my-device@my-domain.com/resource_id'
       to='your-device@your-domain.com'
       id='S0001'>
      <req xmlns='urn:xmpp:iot:sensordata' seqnr='1' momentary='true'/>
   </iq>
{% endhighlight %}

##Read all fields in a node

lorem etc

##Read a specific field in a node

lorem etc

##Best friend restricting the access

lorem etc

###Node
A Thing can model it's content in several "nodes" for example a heatpump can model it's content as the nodes **Pump**, **WaterHeater**, **Compressor** which all can have several fields

###Field
A Thing can have several **fields** every field is a low level value having some type of SI unit such as kWh, temp in F,C or K

[pidgin-ex]: http://im.about.com/od/imfornewusers/ss/pidgin-account-adding-contacts.htm

