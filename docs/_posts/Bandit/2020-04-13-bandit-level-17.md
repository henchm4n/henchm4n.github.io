---
layout: post
title: "OverTheWire: Bandit Level 17"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 17 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 17 of Bandit from OverTheWire Wargames.

We found the password from [level 16](bandit-level-16).

Username: `bandit17`  
Password: `xLYVMN9WE5zQ5vHacb0sZEVqbrp7nBTn`

The information on the website tells us that we have to find the password which is the only line changed between two files.

So let's connect to the machine and list the 2 files.

![](/assets/posts/OverTheWire/Bandit/Bandit17/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit17/picture2.png)

We can see that there are 2 files named `passwords.new` and `passwords.old`. To determine which line has been changed, we can use the `diff` command. This command compares files line by line and will tell us which file has been changed in the new file.

![](/assets/posts/OverTheWire/Bandit/Bandit17/picture3.png)

So we can see that in the old file, the line has been replaced by a new line which is the next levels password.

To continue, please read my Bandit 18 walkthrough. {% include elements/button.html link="bandit-level-18" text="Level 18" %}

Thank you for reading. :+1: