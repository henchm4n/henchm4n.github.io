---
layout: post
title: "OverTheWire: Bandit Level 23"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 23 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 23 of Bandit from OverTheWire Wargames.

We found the password from [level 22](bandit-level-22).

Username: `bandit23`  
Password: `jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n`

The information on the website tells us that there is a cron job running and we should check in `/etc/cron.d/` for the configuration file.  
It also mentions that we need to write our own script which will be a lot of fun. So lets start by SSH-ing into the level and navigating to `/etc/cron.d/`.

![](/assets/posts/OverTheWire/Bandit/Bandit23/picture1.png)  
![](/assets/posts/OverTheWire/Bandit/Bandit23/picture2.png)

So there is a job running for **bandit24** called **cronjob_bandit24** which is the cron job we want to look at. `cat`-ting the file gives the location of the script that is running.

![](/assets/posts/OverTheWire/Bandit/Bandit23/picture3.png)

And `cat`-ting that file gives us a bash script.

![](/assets/posts/OverTheWire/Bandit/Bandit23/picture4.png)

By the looks of the script, it executes all scripts in a certain directory. The directory we want to put our file in is `/var/spool/bandit24` so we can get the next levels password.  
First, we need to create a directory in `/tmp/` so we have a place to write our script and open that script in a text editor.

![](/assets/posts/OverTheWire/Bandit/Bandit23/picture5.png)

The first thing we do when we write a bash script is to put the `#!/bin/bash` on the first row of the file.  
Then we can go about specifying commands to use that make use of the bandit24 script. I will just be using a simple `cat` command which will create a file in tmp with the password in it.

![](/assets/posts/OverTheWire/Bandit/Bandit23/picture6.png)

And that’s my script. Make sure you `chmod 777` the file so its executable by the cron job script. And now we can copy that file into the `/var/spool/bandit24` directory and wait for the cron job to run, which should only take a minute.

![](/assets/posts/OverTheWire/Bandit/Bandit23/picture7.png)

And just like that, we have the password to the next level.

![](/assets/posts/OverTheWire/Bandit/Bandit23/picture8.png)

To continue, please read my Bandit 24 walkthrough. {% include elements/button.html link="bandit-level-24" text="Level 24" %}

Thank you for reading. :+1: