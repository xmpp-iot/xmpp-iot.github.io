---
layout: article
title:  "Friendship between peers"
categories: basics
modified: 2014-11-04T01:01:01
tags: [sample]
toc: true
share: false
comments: false
ads: false
---

The most basic concept of using XMPP or for plain chat. Is the notion of being friends. To exchange data between two endpoints they need to be friends 

#Friend request

The friending process starts with one end point asking another for a "subscription" [Pidgin example][pidgin-ex]
The two enpoints can be in any domains **my-thing@my-domain.com/resource_id** makes a friend request to **your-thing@your-domain.com/**

##Confirm request

The enpoint confirms the request and sends a friend request back to the originating peer

##Dual subscription

The two enpoints now have a dual subscription in talking to each other so they can now send read and write 

# Best friend, Adding security

The usage of friendship is very good if you are a human talking your own descisions  


###JID (jabber id)
Every account in the XMPP network have an identity that looks like an email adress it is a uniqe identifier in the domain this is called the Jabber ID

###Resource_id
For every login to a server a client does it will recive an **Resource_id** this is used to distinguish between for example you being logged in through your ipad, phone, computer etc.
When working with devices it is seldom a device has several resource_id's

[pidgin-ex]: http://im.about.com/od/imfornewusers/ss/pidgin-account-adding-contacts.htm

