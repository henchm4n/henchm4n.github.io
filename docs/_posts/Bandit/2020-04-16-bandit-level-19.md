---
layout: post
title: "OverTheWire: Bandit Level 19"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 19 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 19 of Bandit from OverTheWire Wargames.

We found the password from [level 18](bandit-level-18).

Username: `bandit19`  
Password: `IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x`

The information about the level tells us there is a file in the home directory and we need to use it to access the password for the next level.

So lets SSH into the next level.

![](/assets/posts/OverTheWire/Bandit/Bandit19/picture1.png)  
![](/assets/posts/OverTheWire/Bandit/Bandit19/picture2.png)

We can see an executable file called `bandit20-do`. When we run it, we see that it tells us how to use the executable.

![](/assets/posts/OverTheWire/Bandit/Bandit19/picture3.png)

So we can run commands as another user, cool.

![](/assets/posts/OverTheWire/Bandit/Bandit19/picture4.png)

We can now access bandit20s' password located at `/etc/bandit_pass/bandit20` and `cat` the file.

![](/assets/posts/OverTheWire/Bandit/Bandit19/picture5.png)

To continue, please read my Bandit 20 walkthrough. {% include elements/button.html link="bandit-level-20" text="Level 20" %}

Thank you for reading. :+1: