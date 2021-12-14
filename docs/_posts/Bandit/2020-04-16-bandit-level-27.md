---
layout: post
title: "OverTheWire: Bandit Level 27"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 27 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 27 of Bandit from OverTheWire Wargames.

We found the password from [level 26](bandit-level-26).

Username: `bandit27`  
Password: `3ba3118a22e93127a4ed485be72ef5ea`

The information on the website tells us that we need to use `git` to clone a repository to get the password for the next level.  
So first we will SSH into the level and create a directory in `tmp/`.

![](/assets/posts/OverTheWire/Bandit/Bandit27/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit27/picture2.png)

Now we can use `git` to clone the repository.

![](/assets/posts/OverTheWire/Bandit/Bandit27/picture3.png)

And as we look into the repository, we come across a file called **README** which contains the password for the next level.

![](/assets/posts/OverTheWire/Bandit/Bandit27/picture4.png)

To continue, please read my Bandit 28 walkthrough. {% include elements/button.html link="bandit-level-28" text="Level 28" %}

Thank you for reading. :+1:
