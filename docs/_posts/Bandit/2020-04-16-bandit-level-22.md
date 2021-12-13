---
layout: post
title: "OverTheWire: Bandit Level 22"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 22 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 22 of Bandit from OverTheWire Wargames.

We found the password from [level 21](bandit-level-21).

Username: `bandit22`  
Password: `Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI`

The information tells us that there is cron job running and we should check `/etc/cron.d` for the configuration file.  
So lets SSH into the box and navigate to `/etc/cron.d`.

![](/assets/posts/OverTheWire/Bandit/Bandit22/picture1.png)  
![](/assets/posts/OverTheWire/Bandit/Bandit22/picture2.png)

There is a job for `bandit23` and we can `cat` it to see what script it runs.

![](/assets/posts/OverTheWire/Bandit/Bandit22/picture3.png)

We see a script in `/usr/bin` is run. So lets also `cat` that file to see the script that is running.

![](/assets/posts/OverTheWire/Bandit/Bandit22/picture4.png)

We see a script that declares some variables and copies the next levels password into a tmp file.  
So we need to find out what the variable `mytarget` comes out as. So to do this, we can just type the command into the terminal to get the `md5sum` string.

![](/assets/posts/OverTheWire/Bandit/Bandit22/picture5.png)

Notice that for `myname`, we type in bandit23 as that is the password we are trying to find. Next we just `cat /tmp/8ca319486bfbbc3663ea0fbe81326349` to find the password that was run by the script.

![](/assets/posts/OverTheWire/Bandit/Bandit22/picture6.png)

And we get the next levels password.

To continue, please read my Bandit 23 walkthrough. {% include elements/button.html link="bandit-level-23" text="Level 23" %}

Thank you for reading. :+1: