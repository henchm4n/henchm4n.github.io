---
layout: post
title: "OverTheWire: Bandit Level 32"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 32 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 32 of Bandit from OverTheWire Wargames.

We found the password from [level 31](bandit-level-31).

Username: `bandit32`  
Password: `56a9bf19c63d650ce78e6ec0354ee45e`

The information doesn't tell us any information about the level so we SSH into the level to get started.

![](/assets/posts/OverTheWire/Bandit/Bandit32/picture1.png)

And we are welcomed with an uppercase shell.

![](/assets/posts/OverTheWire/Bandit/Bandit32/picture2.png)

We can try some commands but none of the work.

![](/assets/posts/OverTheWire/Bandit/Bandit32/picture3.png)

The way to get out of this shell is to type `$0` into the terminal. This expands to the name of the shell or the script running the file, letting us call the shell or script again.

![](/assets/posts/OverTheWire/Bandit/Bandit32/picture4.png)

And we see we have escaped the shell and the terminal thinks we are bandit 33 meaning we can cat the password file in `/etc`.

![](/assets/posts/OverTheWire/Bandit/Bandit32/picture5.png)

And that is the password for the next level.

To continue, please read my Bandit 33 walkthrough. {% include elements/button.html link="bandit-level-33" text="Level 33" %}

Thank you for reading. :+1: