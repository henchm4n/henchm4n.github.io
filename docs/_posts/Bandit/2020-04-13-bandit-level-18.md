---
layout: post
title: "OverTheWire: Bandit Level 18"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 18 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 18 of Bandit from OverTheWire Wargames.

We found the password from [level 17](bandit-level-17).

Username: `bandit18`  
Password: `kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd`

As can be seen on the website, there is a file called `readme` stored in the home directory. But it has also told us that we are automatically logged out when we are logged in.

SSH has an option where you can specify commands to run as soon as your computer is connected to the remote machine. And we are going to take advantage of that to `cat` the `readme` file. 

Here is a resource detailing the process: [https://www.cyberciti.biz/faq/unix-linux-execute-command-using-ssh/](https://www.cyberciti.biz/faq/unix-linux-execute-command-using-ssh/).

![](/assets/posts/OverTheWire/Bandit/Bandit18/picture1.png)

As we can see, it returns the contents of the `readme` file and gives us the password for the next level.

To continue, please read my Bandit 19 walkthrough. {% include elements/button.html link="bandit-level-19" text="Level 19" %}

Thank you for reading. :+1: