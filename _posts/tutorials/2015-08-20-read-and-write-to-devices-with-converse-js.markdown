---
layout: article
title: "Read and Write to Devices With Converse.js"
author: adhish_singla
modified:
categories: tutorials
excerpt: Being able to connect to devices directly from a browser is very easy try it out here
tags: [howto]
toc: true
image:
  feature:
  teaser: conversejs.png
  thumb:
share: false
comments: false
ads: false
date: 2015-08-20T23:29:14+05:30
---

This tutorial is regarding using Converse.Js to read values and write values to devices, and also retrieve history of fields.

## Getting Started

Follow the instructions given [here](https://conversejs.org/docs/html/quickstart.html)

Use this [converse.js file](https://github.com/adhish20/converse.js/blob/dev_iot/builds/converse.js) instead of the one given in above link.

## Start with logging into an XMPP account

* Log into your xmpp account.

* Contacts  will be displayed with an Icon to their left.

* These icons determine the type of contacts (Sensor Devices, Control Devices or Contacts)

* Open a Chatbox with a Device.

* We have used [Command Feature](https://conversejs.org/docs/html/features.html#commands) to implement the functions.

## Reading Values from a Device

* It works for Sensor as well as Control Devices.

* The command for reading a value is '/read'.

* It will display the fields stored in the device along with their present values. Like this :

![Read Requests](/images/read.png)

## Writing Value to a Field

* It works for Control Devices.

* First perform a Read to know the FieldNames.

* The command for writing a Value to a FieldName is '/write FieldName Value'.

* Now you can again perform a Read to check if the Value for that FieldName is changed. Like this :

![Write Requests Step-1](/images/write1.png)
![Write Requests Step-2](/images/write2.png)
![Write Requests Step-3](/images/write3.png)

## History Retrieval for a Field

* It works for Sensor as well as Control Devices for Fields that store their History.

* The command to  retrieve Hisotry of a FieldName is '/history day/week/month/year FieldName'.

* Output for the same looks like this:

![History Requests Step-1](/images/history1.png)
![History Requests Step-2](/images/history2.png)
![History Requests Step-3](/images/history3.png)

Hope you like playing around with it :)
