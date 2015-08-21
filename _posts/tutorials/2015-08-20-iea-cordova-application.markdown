---
layout: article
title: "IEA Cordova Application"
author: adhish_singla
modified:
categories: tutorials
excerpt:
tags: [howto]
toc: true
image:
  feature:
  teaser: cordova_logo.png
  thumb:
share: false
comments: false
ads: false
date: 2015-08-20T11:38:53+05:30
---

This tutorial is regarding using IEA Cordova Mobile Application, which can be used to read values and write values to devices, and also retrieve history of fields.

## Getting Started

* You need to install the application to your android device using latest apk file.
* Home page looks like this : 

<img src="/images/login2.png" alt="Login View" width="360" />

## Start with logging into an XMPP account

* Login with any xmpp account. Online contacts along with the details of device, will be displayed for the contacts like this:

<img src="/images/contacts2.png" alt="Retrieved Contacts VCard Display" width="360" />

## Reading Values from a Device

* Clicking on a device contact will perform a Read Operation, the fields stored in the device along with their value will appear as a drop down for the contact:

<img src="/images/read-mobile1.png" alt="Read Values of a Device" width="360" />

## Writing Value to a Field

* If a field is writable, we can edit its value and tap the 'write' button, to send a write to a field request to the device:

<img src="/images/write-mobile1.png" alt="Write for App" width="360" />

## History Retrieval for a Field

* If a field stores history of its values, tapping on the 'fieldname' will generate a graph based on the history of its values:

<img src="/images/history-mobile2.png" alt="History Graph 1" width="360" />
<img src="/images/history-mobile1.png" alt="History Graph 2" width="360" />

Hope you like playing around with it :)