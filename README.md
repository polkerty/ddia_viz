# A playful learning tool for DDIA (Designing Data-Intensive Applications)
I'm currently reading through the book _Designing Data-Intensive Applications_.

As of 1/31/24, I'm about 360 pages through ~550 pages of content. A reasonable sitting is 1 hour per day for about 20 pages of content. I'm  currentlly in chapter 9, reading about consensus / 2 phase commit / etc.
(This is chewy material; I find myself slowing down as the hour goes on -- don't win much by trying to push through it too fast.)

Because the material is so interesting and dense-with-ideas (though not dense-in-expositional-style), I need some additional ways to let the material soak in. One way is to review a bit of the previous day's reading; better still is to try to explain the material out loud, later; and even better what I'm doing here:

Making playful simulations and visualizations of the distributed system described in the books.

So far (as of 1/31/24), this contains:

* A visualization of a topology of servers and network links. The servers are placed in a circle, and any of them can be directly connected by a network link.
* A concept of "time", which influences message-passing over the network: network links have latency (how long it takes a message to pass through) and bandwidth (how many messages can pass through at once).
* An implementation of a gossip protocol for propagating key-value stores with dotted version vectors to track causality relationships
and conflicts. I found [this post from Riak](https://riak.com/posts/technical/vector-clocks-revisited-part-2-dotted-version-vectors/index.html?p=9929.html) helpful. There are still some bugs I'm working out.

## Technical notes
In order to have the most fun here, I'm implementing the code and visualizations as I used to do 10 years ago. A single
HTML file with embedded JS and CSS, no frameworks like React, no visualization libraries like d3.js or Plotly, no web
technologies I don't enjoy such as HTML Canvas. It's all raw JS classes, CSS, and eg algebra, trignonometry, translations, and rotations to implement the geometrical aspects.

As such, I'm optimizing this code for my own fun and productivity, not for any one else to read or contribute. If I learn anything,
it will be from reflecting on the material and procedures of DDIA as I do this, not from any web technology I use to implement this specific HTML simulation.

I may be able to embed this file in some expositional blog post down the line -- that is the only way this work would be of use to 
anyone but myself.

## What's next?
There are a lot of interesting options to implement in this book. I'm considering implementing
2 phase locking and/or 2 phase commit next (very different protocols/purposes, but not too
hard to understand and they implement some very useful guarantees.)
