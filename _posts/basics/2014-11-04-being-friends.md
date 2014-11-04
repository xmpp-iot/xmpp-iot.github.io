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

##Friend request

The friending process starts with one end point asking another for a "subscription" [Pidgin example][pidgin-ex]
The two enpoints can be in any domains **my-thing@my-domain.com/resource_id** makes a friend request to **your-thing@your-domain.com/**

##Confirm request

The enpoint confirms the request and sends a friend request back to the originating peer

##Dual subscription

The two enpoints now have a dual subscription in talking to each other so they can now send read and write 

##Having a Parent, Adding security

The usage of friendship is very good if you are a human talking our own descisions. But if whe are a temp sensor we must talk to a trusted friend to ask for permissions.

> Every device can have a "best friend" or "parent" which is the trusted party that takes the descisions regarding the device possibilities to respond to friendship requests and access to specific fields.

Using this way of endpoint security creates andless possibilities with changing the ownership of devcices during first commissioning[^commission] It even supports the usecase of thirdparty delivering unnamed Things that you can buy and the transfer them to be your own property

[^commission] The process when a Thing recieves it first condiguration.

`JID (jabber id):` Every account in the XMPP network have an identity that looks like an email adress it is a uniqe identifier in the domain this is called the Jabber ID or **JID**. 
{: .notice-inverse}
`Resource:` For every login to a server a client will recive a **Resource** this id is used to distinguish between the different session. For example you being logged in to the same account from your *ipad*, *phone*, *computer* etc.
When working with Things it is seldom a Thing has several logins and resources but you should be aware of the possibility. 
{: .notice-inverse}

[pidgin-ex]: http://im.about.com/od/imfornewusers/ss/pidgin-account-adding-contacts.htm


