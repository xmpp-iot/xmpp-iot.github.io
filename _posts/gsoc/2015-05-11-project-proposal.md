---
layout: article
title: "Prototyping Tools for IoT - Project Proposal"
author: adhish_singla
modified:
categories: gsoc
excerpt:
tags: []
image:
  feature: 
  teaser: prototyping-iot_400x250.png
  thumb:
ads: false
date: 2015-05-11T16:50:57+05:30
---

##Abstract

Internet of Things(IoT) is expected to offer advanced connectivity of devices, systems, and services that goes beyond machine-to-machine communications (M2M) and covers a variety of protocols, domains, and applications. We aim at making Tools and create a binding between SleekXMPP and various Devices like Netatmo,intel edison, intel galileo, raspberry PI 2, beagle bone black, etc. which can be controlled by means of Client Applications. Also to check compatibility between Devices, i.e. if they can Talk(exchange Data) between each other.

##Description and Research

The Project contains mainly 6 deliverables, those are:

1. A web html/javascript based client that is used to visualise and control the devices created.
2. Python scripts toolkit to be run on different devices like raspberry pi, Netatmo etc.
3. An Access Rights Manager that manages what devices can talk to each other.
4. Adding Tutorials to xmpp-iot.org site for showing the wrking of above mentioned.
5. Client-Device Logger that Logs the data of the Device.
6. Implement a first version of the [XEP-0326](http://xmpp.org/extensions/xep-0326.html)

####1. Web Visualization Client

The web client is a html, javascript xmpp client implemented using Strophe that connect to the xmpp network and through the roster it retrieves its friendship subscriptions that it uses to access xmpp endpoints that is devices.

The Javascript is a web Client used to:

* Visualize data with graphs.
* Reading values on demand.
* Sending control commands to change values in the devices.

Use of [Cordova](http://cordova.apache.org/) in combination makes it possible to deliver the client as an native mobile application.

It runs programs and access data that is stored on the server. Since we are working with Internet of Things(IoT), The device would act as a server for the Client Application where the Client would ask for values from the Device and can also receive Events from the Device.

####2. Python Scripts Toolkit for different Devices

Develop Binding between SleekXMPP and Devices for IoT with easy to use example scripts that serves as the Prototyping Tools. When somebody starts to create a device, they can use these scripts as the base for their devices.

Functions needed by an IoT Device are :

* Local Storage for Storage of Data and Values.
* Easy Configurable I/O Management.
* Type Conversions.
* Access Security who can retrieve what Information.

####3. Access Rights Manager

An application that would check for compatibility between Devices and making the exchange of Data more Secure, i.e. who can access what in which device is managed by this application. All this is according to Provisioning Things as in [XEP-0324](http://xmpp.org/extensions/xep-0324.html).

####4. Tutorials

This would generally consist of Videos or Walkthroughs that can guide users on how to work with the Products that are being made as a part of the Project. which will be put on the [XMPP-IoT](http://xmpp-iot.github.io/) site.

####5. Client-Device Logs

A Network Storage that stores logs for “If you make friend with some client it will start logging data for your device”.

####6. First Implementation of XEP-0326

First Implementation of Hiding legacy systems through Concentrators as given in [XEP-0326](http://xmpp.org/extensions/xep-0326.html).

##Approach

My initial work would deal with going through XEP-0323,  XEP-0325, XEP-0324 and XEP-0326 which explains how Reading of Things, Writing of Things, Provisioning of Things and Hiding Legacy systems through Concentrators respectively is done. That would form the basis of how the interaction between the devices work. The most complex task would be to create a good user interface that can be a base for others to build on and therefore i will provide more time to this. This would be my methodology of approaching the Project by learning more and more about it and making it the basis of my Implementation.


There might be need of few external Libraries and APIs like for the Client we need Apache Cordova and Strophe and for Device Toolkits, I need to make API of devices that might include some external library depending upon its functionality.

##Timeline

#####Community Bonding Period

Work on necessary documentation for understanding the Architectural and Functional requirements and design of the Deliverables and Come up with a definitive list of Devices. A primary list of Devices consists of intel edison, intel galileo, raspberry PI 2, beagle bone black.

#####Week 1-2( 25 May - 7 June )

Create an Interactive user interface for Web Visualisation Client using HTML, CSS.

#####Week 3( 8 June - 14 June )

Graph Visualiser for Web Client and extending Teaser Tasks(Relay and Make Friend Features) to the Web View.

#####Week 4( 15 June - 21 June )

Extending existing examples to other hardware platforms like for intel edison, intel galileo, raspberry PI 2, beagle bone black, etc.

#####Week 5( 22 June - 28 June )

Come up with a working HTML Client for devices and Access Rights Manager.

#####Week 6( 29 June - 5 July )

Catch Up for Mid Term Evaluation.

#####Week 7-8( 6 July - 19 July )

Make Web Client as Mobile Application using Cordova.

#####Week 9( 20 July - 26 July )

Create a Client-Device Logger that would log data for a device.

#####Week 10-11( 27 July - 8 August )

Make Tutorials and Implement XEP-0326.

#####Week 12( 10 August - 16 August )

Catch Up Week for all Deliverables.

#####Week 13( 17 August - 23 August )

Pencils Down Week, Improve Documentation for all the Products.

##Project Blog

All related stuff and Updates can be found at the [XMPP IoT-GSoC Blog](http://xmpp-iot.github.io/gsoc/).
