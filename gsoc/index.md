---
layout: article
title: "Gsoc 2015"
date: 2015-03-001T09:44:20-04:00
modified:
categories: 
excerpt: "XMPP-IoT in the Google summer of code 2015"
image:
  feature:
  teaser:
  thumb:
share: true
ads: false
---

The XMPP community is part of the Google summer of Code 2015 and for XMPP-IoT we have several projects

#What is this XMPP-IoT
There are many many solutions to connecting Internet of Things (IoT) devices to internet, to create services and interesting applications. on this site you find an introduction to how we mimic the world of people chatting to enable **any device to any device** interoperability. Supporting all usecases that IoT needs. Especially the possibility to be a way for companies to interact through federation.
The projects are:

* [prototyping tools with python and javascript](http://wiki.xmpp.org/web/Summer_of_Code_2015#Prototyping_tools.2C_for_Internet_of_Things_Using_SleekXMPP_and_Web)
* [Adding XMPP-iot to opent](http://wiki.xmpp.org/web/Summer_of_Code_2015#Adding_XMPP-IoT_to_the_openHAB_smarthome_project_using_Smack)

The third IoT realted project is maintained by Process one

* [Provisioning and registry of Things for Ejabberd](http://wiki.xmpp.org/web/Summer_of_Code_2015#Provisioning_and_registry_of_Things_.28IoT.29_for_ejabberd)
You can also propose others if you have an idea. post it to the chat room or mailing list

#Talk to us!

- We'd really like to talk with you a bit, so please come by the XSF's GSoC MUC room at gsoc@muc.xmpp.org and have a chat. [you find the logs here]( http://logs.xmpp.org/gsoc)
-  [Join the gsoc maillist]( http://mail.jabber.org/mailman/listinfo/gsoc)
- there is also a twitter handle [@XMPPIoT to be used](https://twitter.com/XMPPIoT)

##Teaser task for prototyping tools

To be able to quickly startup any project you need to have prototyping tools. Using python and javascript in combination gives you a very quick start on almost any device

* Run the sample scripts under the [Tutorials](http://xmpp-iot.github.io/tutorials/) And propose better ones to understand the concepts.
* Create a python script "makingfriends" to manage friendship subscriptions between devices when you need several JID's to be able to talk to each other.
* Build a one to many chat room example of a device sending values to many devices in a MUC chatroom using XEP323 message stanzas
* Look at the scripts avaliable in the [SleekXMPP IoT examples](https://github.com/joachimlindborg/SleekXMPP/tree/xep_0323_325/examples/IoT) especially the PhilipsHue. Create a mapping to another open API for a device.


##Teaser task for openHAB

* start an OpenHAB instance and trigger the XMPP module to send a plain chat message to the python script in the tutorial triggering a relay "Toggle"
* Implement a first SMACK-extension for the XEP323 basic stanza  

This is maintained by [Joachim Lindborg](http://lsys.se/)  member of the  [XMPP Extensions Foundation](http://xmpp.org/about-xmpp/xsf/xsf-member-list/)
