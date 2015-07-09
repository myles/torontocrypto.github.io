---
title: How our IRC chat bot helps you talk to us anonymously
date: 2015-07-09 11:00:00 EDT
category: blog
author: m
---

The people in and around Toronto Crypto do a lot of talking over IRC.
It's an easy way to ask and answer questions, plan events,
and banter about current goings-on in information security.
But IRC itself isn't a private or secure method of communication.
If we're providing a forum for conversation about privacy,
doesn't it make sense to offer a channel that respects it?

Our most-used channel is __#torontocrypto__ on [OFTC](http://www.oftc.net/).
OFTC is a great hub for technical topics, but as with any open network,
there are lots of ways that your identity can be connected to your conversations.
If you're a tinfoil-hat type person (some of our best friends are!),
or you have a specific need for anonymity,
or you just haven't given up your natural desire for privacy,
you may be averse to joining an IRC channel in the clearnet.
Sure, you can connect with HTTPS so your packets can't be sniffed in transit,
and if you register with OFTC's NickServ they'll even cloak your IP from whois calls.
But your client still leaks a lot of information,
and you're trusting the network itself with even more.

### Chatting in the dark

So we took inspiration from [I2P](https://en.wikipedia.org/wiki/I2P),
aka the Invisible Internet Project.
I2P is an anonymizing network, [similar to Tor](https://geti2p.net/en/comparison/tor)
but with tighter protection against leaking client information.

I2P's main IRC network, __IRC2P__, is similar to other IRC networks
but it only accepts connections through I2P.
This means that significantly less of IRC2P users' identifying information is exposed
to other users, and to the server itself.
If you're connected to I2P, you can access IRC2P with your IRC client at localhost port __6668__.

To serve these users, we started a __#torontocrypto__ channel on the IRC2P network.
Anyone with a healthy paranoia about the clearnet can log in here,
and not feel like they're getting their ID card scanned at the door.
But what good is that if all the conversation is happening over in the OFTC channel?

### Enter Borgil

This is one of the reasons we created [Borgil](https://github.com/torontocrypto/borgil),
a bot you may see mingling with the humans in our channel.
Mostly known for spouting links from our favourite RSS feeds,
or running searches for us when we're too lazy to switch windows,
Borgil also serves as a relay between the sunny side of our chatroom and the shadowy corners.

Our trusty chatbot logs into both OFTC and IRC2P, and sits in both channels.
When he hears a message in one channel, he immediately echoes it out loud in the other.
This way, the two rooms share the same conversation,
but no identifying information other than usernames are passed from one to the other.
The I2P folks have a similar setup for their __#i2p__ channels, which are also on OFTC and IRC2P.

This gives you a bit more choice in your balance of convenience and security,
but of course, there are still risks to be aware of.
Your messages could be correlated with other communications you might be making at the same time,
for instance.
If you click links from chat, they may open in the clearweb with your unprotected browser.
You should already have these kinds of considerations in mind, though,
when using anonymizers like I2P or Tor.

So if you'd like to chat with us but want to stay in the shadows of the darknet,
come to #torontocrypto on I2P and say hi. Borgil will pass it on. :)

> By the way:
[the I2P team is hosting a meetup](https://geti2p.net/en/blog/post/2015/06/02/Toronto-Meetup)
in Toronto next month.
It will be on August 15-16, 2015 at the mighty [Hacklab](https://hacklab.to/),
and we will be there!
