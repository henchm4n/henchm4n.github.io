---
layout: post
title: "OverTheWire: Bandit Level 10"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 10 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 10 of Bandit from OverTheWire Wargames.

We found the password from [level 9](bandit-level-9).

Username: `bandit10`  
Password: `truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk`

The information tells us that `data.txt` is encoded in `base64`.

First lets SSH into the box and cat data.txt to see what's stored in the file.

![](/assets/posts/OverTheWire/Bandit/Bandit10/picture1.png)  
![](/assets/posts/OverTheWire/Bandit/Bandit10/picture2.png)

Bash gives us a function we can use in order to encode and decode base64 called `base64`. We could in theory, just google base64 decoder and copy the string into that. But it is often quicker to use pipes.
To use the base64 function to decode data, we need to use the `-d` option for decode

![](/assets/posts/OverTheWire/Bandit/Bandit10/picture3.png)

So the final command is given as:

![](/assets/posts/OverTheWire/Bandit/Bandit10/picture4.png)

Which gives us the password to the next level.

To continue, please read my Bandit 11 walkthrough. {% include elements/button.html link="bandit-level-11" text="Level 11" %}

Thank you for reading. :+1: