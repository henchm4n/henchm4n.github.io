---
layout: post
title: "OverTheWire: Bandit Level 21"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 21 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 21 of Bandit from OverTheWire Wargames.

We found the password from [level 20](bandit-level-20).

Username: `bandit21`  
Password: `gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr`

The information given to us on the website says that there are programs running at regular intervals and we should look in `/etc/cron.d/` for the configuration file and see what command is being executed.

![](/assets/posts/OverTheWire/Bandit/Bandit21/picture1.png)  

Now that we are in, let's have a look in `/etc/cron.d/`.

![](/assets/posts/OverTheWire/Bandit/Bandit21/picture2.png)

As we can see in the directory, there are a number of jobs that are running. We are interested in `cronjob_bandit22`. So we can `cat` the file to see what command is running.

![](/assets/posts/OverTheWire/Bandit/Bandit21/picture3.png)

We see that it runs the script and sends **stderr** to `/dev/null`. So lets have a look at the script and see what it contains.

![](/assets/posts/OverTheWire/Bandit/Bandit21/picture4.png)

The script creates a file in `tmp` and copies `level22` password into the file. Opening the tmp file should give us the password to the next level.

![](/assets/posts/OverTheWire/Bandit/Bandit21/picture5.png)

To continue, please read my Bandit 22 walkthrough. {% include elements/button.html link="bandit-level-22" text="Level 22" %}

Thank you for reading. :+1: