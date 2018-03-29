---
title: Censorship Resistance or\: How I Stopped Worrying and Learned to Rendezvous
date: 2018-03-24 01:30:00+09:00
description: My thoughts on resistance
tags: [ "Censorship" ]
aliases:
- /2018/03/24/rendezvous
---

This post is all about my thoughts on rendezvous protocols. 

Networks are nothing more than a bunch of computers connected to one another. Before joining a network, one needs to be able to even figure out how to join it. For the web, we have things like domain names and DNS that translate websites we found on search engines into IP addresses which act as the doors to join a network. This is what a rendezvous is. A way for your computer to find another computer to connect to in order to join a network.

In normal conditions, DNS is fine to use as a rendezvous protocol. It is simple and decentralized. There is great tooling for it, and the entire world supports it. [DNS is even used](http://awesome.datproject.org/dns-discovery) in decentralized and distributed network scenarios. However, things start changing when trying to access a blocked network in a censored region. 

Even though DNS is decentralized, default DNS resolvers can block requests for censored domain names. DNS requests to other non-censoring DNS reolvers can also be blocked. It seems to me that DNS isn't well suited for rendezvous in hostile conditions. 

For setting up a successful rendezvous protocol in a censored environment, I think there need to be certain things in place. 

It seems to me that the best way to access information in a heavily censored environment is to look at it through an economic perspective. If there is a company outside of the censored region that allows for user submission, and it operates a secure connection channel like TLS, that seems to be the perfect candidate to perform rendezvous. 
Since the organization operating the censored region gains massive economic incentives from keeping that company's websites un-censored, one can use that to their advantage and host a rendezvous system within it.

In rendezvous, one of the most worrying issues is the issue of trust. How can one make sure that the network they are connecting to is the actual network they want to connect to? How can they make sure the rendezvous point is actually legitimate? This is something that is an open-problem 


## Interesting projects in rendezvous

[meek](https://trac.torproject.org/projects/tor/wiki/doc/meek) - connect to a Tor node via domain fronting. 

[Flash Proxy](https://crypto.stanford.edu/flashproxy/flashproxy.pdf) - short lived and abundant proxies 

