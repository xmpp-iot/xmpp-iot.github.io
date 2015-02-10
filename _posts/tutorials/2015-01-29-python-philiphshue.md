---
layout: article
title:  "Being friend with  Philips Hue lights"
categories: tutorials
modified: 2015-01-29T01:01:01
tags: [howto]
toc: true
image:
 teaser: python-logo@2x.png 
share: false
comments: false
ads: false
---


This tutorial runs a python script on a raspberry, or the like, and publishes a XMPP JID that you can use to 
# Preparations
you need an environment that can run python scripts.

## Setup a JID for each lamp
first setup accounts for each lamp on your favourite XMPP site for example jabber.se

## Get the python code

Clone the philipshue api and SleekXMPP code from github

{% highlight bash session %}
>$ git clone https://github.com/studioimaginaire/phue.git
Cloning into 'phue'...

>$ git clone -b xep_0323_325 https://github.com/joachimlindborg/SleekXMPP.git
Cloning into 'SleekXMPP'...
{% endhighlight %}


## start the server device

The script will try to connect to the local HUE gateway. If it cannot get access the script will ask you to push the connect button. If It is able to connect it will log on to the gateway.

- Each lamp is known as "individual" so you start one script for each lamp.
- If you don't provide an individual you will adress the whole group
  of lamps connected to the hue gateway

when the script starts the first time you need to press the button on
the Philipshue gateway to open access to it. Use a - - debug to get
more information

{% highlight bash session %}
>$ cd SleekXMPP/examples/IoT/
>$ python IoT_PhilipsHueApi.py -j john@your.domain.com -p password -n “John” --individual 1

INFO     Negotiating TLS
INFO     Using SSL version: 3
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate COULD NOT BE VERIFIED.
INFO     JID set to:  john@your.domain.com/544301500141697366520183
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate
expiration COULD NOT BE VERIFIED.


{% endhighlight %}

you can now start chatting with the lamp by sending **hi** or **?** in
the chat window.

{% highlight bash session %}
>$ cd SleekXMPP/examples/IoT/
>$ python IoT_PhilipsHueApi.py -j john@your.domain.com -p password -n “John” --individual 1

INFO     Negotiating TLS
INFO     Using SSL version: 3
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate COULD NOT BE VERIFIED.
INFO     JID set to:  john@your.domain.com/544301500141697366520183
WARNING  Could not find pyasn1 and pyasn1_modules. SSL certificate
expiration COULD NOT BE VERIFIED.


{% endhighlight %}
giving a debug flag would give more information

# Reading a value from a device
We now start a script that continiously reads values from the first.

# Writing a value to a device
keep the two scripts above running ans start a third one changing values in the sever device. 
