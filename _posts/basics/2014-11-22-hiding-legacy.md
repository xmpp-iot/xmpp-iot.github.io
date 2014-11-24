---
layout: article
title: "Hiding legacy"
categories: basics
modified: 2014-11-24T11:57:41-04:00
tags: [basics]
toc: false
comments: false
ads: false
---

When talking to a peer you can assume it is a device or thing with node's and fields. But behind that device there could be a whole legacy system. What if the peer you are talking to is a big legacy system consisting of thousands of devices with many fields.

XMPP-IoT give you the possibility to model your world in different ways we have talked of **Nodes** and **Fields** and that a device can have a flat level with many nodes with fields

The XMPP-IoT extension [XEP-326 Concentrators](http://xmpp.org/extensions/xep-0326.html) makes it possible to extend this with the possibility to describe any hiearchy physical and or logical.

This makes it possible for a peer to investigate another peer and learn about the hiearchy of nodes and fields.

##example hiding a legacy modbus system

Modbus is a communication bus used in many industrial systems.



*pic on the setup*


We now model every device on the Modbus bus as a separate Node with Fields under a Datasource called Modbus

