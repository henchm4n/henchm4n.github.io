---
layout: post
title: "OverTheWire: Bandit Level 9"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 9 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 9 of Bandit from OverTheWire Wargames.

We found the password from [level 8](bandit-level-8).

Username: `bandit9`  
Password: `UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR`

From the information given on the website, we know that we need to search the `data.txt` file for several '=' characters.

So lets start by SSH-ing into the box and listing the home directory.

![](/assets/posts/OverTheWire/Bandit/Bandit9/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit9/picture2.png)

The strange thing is though, when we try and `cat` or `les`s the file, `cat` doesn't produce and output and `less` tells us it may be a binary file.

![](/assets/posts/OverTheWire/Bandit/Bandit9/picture3.png)

When we run the `file` command, we see that `data.txt` is in fact just data.

![](/assets/posts/OverTheWire/Bandit/Bandit9/picture4.png)

The wording of the goal gives it away a bit, but a command that is used to search through this type of data is called `strings`. The purpose of this function is to comb through the data in search of readable strings.
So when we run the command against `data.txt`, we get output of all readable strings in the file.

![](/assets/posts/OverTheWire/Bandit/Bandit9/picture5.png)

Using what we learnt from pipes and `grep`, we can search the output of the strings command for lines containing multiple '=' characters.

![](/assets/posts/OverTheWire/Bandit/Bandit9/picture6.png)

And we are given the password to the next level.

To continue, please read my Bandit 10 walkthrough. {% include elements/button.html link="bandit-level-10" text="Level 10" %}

Thank you for reading. :+1: