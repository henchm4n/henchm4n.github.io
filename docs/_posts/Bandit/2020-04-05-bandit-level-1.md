---
layout: post
title: "OverTheWire: Bandit Level 1"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 1 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 1 of Bandit from OverTheWire Wargames.

We found the password from [level 0](bandit-level-0).

Username: `bandit1`  
Password: `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`

SSH into the box, using the password found in the previous level.

![](/assets/posts/OverTheWire/Bandit/Bandit1/picture1.png)

We start with an `ls` of the home folder.

![](/assets/posts/OverTheWire/Bandit/Bandit1/picture2.png)

When we try and cat the file like the previous level, it just leaves us on hold and doesn't open anything.

![](/assets/posts/OverTheWire/Bandit/Bandit1/picture3.png)

In order to read this file, we need to prefix the filename with a path.  
Here is a good resource that informs us of why this is the case > [https://unix.stackexchange.com/questions/16357/usage-of-dash-in-place-of-a-filename](https://unix.stackexchange.com/questions/16357/usage-of-dash-in-place-of-a-filename)  
Doing so gets us the password.

![](/assets/posts/OverTheWire/Bandit/Bandit1/picture4.png)

To continue, please read my Bandit 2 walkthrough. {% include elements/button.html link="bandit-level-2" text="Level 2" %}

Thank you for reading. :+1: