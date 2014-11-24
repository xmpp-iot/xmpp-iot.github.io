---
layout: article
title: "Datamodel of things"
categories: basics
modified: 2014-11-20T11:57:41-04:00
tags: [basics]
toc: true
comments: false
ads: false
---

In XMPP-IoT we have restricted a device to have a flat model consisting of one or many  **Node** and each Node can have several **Fields**. Each field conforms to a readable or writable value with an SI unit.

If you would like to create a more complex device with recursive defintions of nodes you should describe them as a concentrator wich also is used to hide legacy systems. 

## Node
A node is a logical group of field with a unique name in the 

## Field
