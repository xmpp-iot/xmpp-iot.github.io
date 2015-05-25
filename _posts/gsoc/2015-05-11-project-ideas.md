---
layout: article
title: "Project Ideas"
modified:
categories: gsoc
excerpt:
tags: []
image:
  feature: 
  teaser: prototyping-iot_400x250.png
  thumb:
ads: false
date: 2015-05-11T15:02:23+05:30
---

The XMPP community is part of the Google summer of Code 2015 and for XMPP-IoT we have several projects

#What is this XMPP-IoT
There are many solutions how to connect Internet of Things (IoT) devices to internet, to create services and interesting applications. on this site you find an introduction to how we mimic the world of people chatting to enable **any device to any device** interoperability. Supporting all usecases that IoT needs. Especially the possibility to be a way for companies to interact through federation.

The projects are:

* [prototyping tools with python and javascript](http://wiki.xmpp.org/web/Summer_of_Code_2015#Prototyping_tools.2C_for_Internet_of_Things_Using_SleekXMPP_and_Web)
* [Adding XMPP-iot to openHAB using java SMACK](http://wiki.xmpp.org/web/Summer_of_Code_2015#Adding_XMPP-IoT_to_the_openHAB_smarthome_project_using_Smack)

The third IoT realted project is maintained by Process one

* [Provisioning and registry of Things for Ejabberd](http://wiki.xmpp.org/web/Summer_of_Code_2015#Provisioning_and_registry_of_Things_.28IoT.29_for_ejabberd)

You can also propose others if you have an idea. post it to the chat room or mailing list

#Talk to us!

- We'd really like to talk with you a bit, so please come by the XSF's GSoC MUC room at gsoc@muc.xmpp.org and have a chat. [you find the logs here]( http://logs.xmpp.org/gsoc)
-  [Join the gsoc maillist]( http://mail.jabber.org/mailman/listinfo/gsoc)
- there is also a twitter handle [@XMPPIoT to be used](https://twitter.com/XMPPIoT)

##Teaser tasks for prototyping tools

To be able to quickly startup any project you need to have prototyping tools. Using python and javascript in combination gives you a very quick start on almost any device

* Run the sample scripts under the [Tutorials](http://xmpp-iot.github.io/tutorials/) And propose better ones to understand the concepts.
* Create a python script "makingfriends" to manage friendship subscriptions between devices when you need several JID's to be able to talk to each other.
* Build a one to many chat room example of a device sending values to many devices in a MUC chatroom using XEP323 message stanzas
* Look at the scripts avaliable in the [SleekXMPP IoT examples](https://github.com/joachimlindborg/SleekXMPP/tree/xep_0323_325/examples/IoT) especially the PhilipsHue. Create a mapping to another open API for a device.


##Teaser tasks for openHAB

 [OpenHAB](http://openhab.org/) is an opensoruce project acting as a control environment for a smart home bridging between many different physical protocols. 

* start an OpenHAB instance and trigger the XMPP module to send a plain chat message **ex "Toggle"** or **"relay=True"**.  This can be sent to another OpenHAB instance recieving the message and acting on it's local variables. It can also be sent to the  [python script in the tutorial](http://xmpp-iot.github.io/tutorials/python-tutorial/) triggering a relay to "Toggle".

* Implement a first SMACK-extension for the  [XEP323 basic stanzas]( http://xmpp.org/extensions/xep-0323.html). First a read request.   [Smack extensions](https://github.com/igniterealtime/Smack/tree/master/smack-extensions) some more info [Smack docs](https://www.igniterealtime.org/builds/smack/docs/latest/documentation/extensions/index.html)

This is maintained by [Joachim Lindborg](http://lsys.se/)  member of the  [XMPP Extensions Foundation](http://xmpp.org/about-xmpp/xsf/xsf-member-list/)

