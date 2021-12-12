---
layout: post
title: "OverTheWire: Bandit Level 7"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 7 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 7 of Bandit from OverTheWire Wargames.

We found the password from [level 6](bandit-level-6).

Username: `bandit7`  
Password: `HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs`

The information on the website tells us that the password is stored in the file `data.txt` next to the word `millionth`.

Let's start by SSH-ing into the box and we see that `data.txt` is in the home directory.

![](/assets/posts/OverTheWire/Bandit/Bandit7/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit7/picture2.png)

The first thing we notice is that the file has 4 million bytes.  
Instead of using `cat` and having the screen filled with information, we can use a command `less`, which limits the amount shown on screen at any time. This is the same command that is called if you were looking up a man page and makes it easy to navigate a file.

When we `less` the file, we see it is filled with word password pairs and would take a long time to go through each line in search of the word `millionth`.

![](/assets/posts/OverTheWire/Bandit/Bandit7/picture3.png)
![](/assets/posts/OverTheWire/Bandit/Bandit7/picture4.png)

This is where the command `grep` comes in which can search a file for a particular string of characters.  
So when we search the file using `grep` and the string equal to `millionth`, it finds the line containing `millionth` and pulls out the line, including the password.

![](/assets/posts/OverTheWire/Bandit/Bandit7/picture5.png)

To continue, please read my Bandit 8 walkthrough. {% include elements/button.html link="bandit-level-8" text="Level 8" %}

Thank you for reading. :+1: