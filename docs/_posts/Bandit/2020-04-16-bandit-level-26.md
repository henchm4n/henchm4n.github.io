---
layout: post
title: "OverTheWire: Bandit Level 26"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 26 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 26 of Bandit from OverTheWire Wargames.

We found the password from [level 25](bandit-level-25).

Username: `bandit26`  
Password: `5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z`

I am assuming that you already have a shell on bandit26 as in order to get the shell, you need to go through level25. If you need help, just follow my tutorial on [level 25](bandit-level-25) to refresh your memory.

The information on the website just states we need to get the password for bandit27. So let's use the shell we got from the past level and list the files in the home directory.

![](/assets/posts/OverTheWire/Bandit/Bandit26/picture1.png)

We see that there is an executable file called `bandit27-do`. We can run the file to see what sort of messages it provides us.

![](/assets/posts/OverTheWire/Bandit/Bandit26/picture2.png)

This seems oddly family with the command for level 19. So lets cat the password in `/etc/bandit_pass/bandit27`.

![](/assets/posts/OverTheWire/Bandit/Bandit26/picture3.png)

And we are given the password to the next level.

To continue, please read my Bandit 27 walkthrough. {% include elements/button.html link="bandit-level-27" text="Level 27" %}

Thank you for reading. :+1: