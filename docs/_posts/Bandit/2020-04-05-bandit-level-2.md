---
layout: post
title: "OverTheWire: Bandit Level 2"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 2 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 1 of Bandit from OverTheWire Wargames.

We found the password from [level 1](bandit-level-1).

Username: `bandit2`  
Password: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`

SSH into the box.

![](/assets/posts/OverTheWire/Bandit/Bandit2/Picture1.png)

Doing `ls` lists what looks like multiple files.
But if we use the `-l` (dash L) option, which uses a long listing format, we see that it is in fact a file with spaces in its name.

![](/assets/posts/OverTheWire/Bandit/Bandit2/Picture2.png)

There are many ways to deal with files that have spaces in their filename. Two of the most common ways are:  
1\. To surround the filename with quotes or double quotes.

![](/assets/posts/OverTheWire/Bandit/Bandit2/Picture3.png)

2\. To use escape characters.

![](/assets/posts/OverTheWire/Bandit/Bandit2/Picture4.png)

This guide here gives a good explanation on quotes and escape characters > 
[https://www.tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_03.html](https://www.tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_03.html)

To continue, please read my Bandit 3 walkthrough. {% include elements/button.html link="bandit-level-3" text="Level 3" %}

Thank you for reading. :+1: