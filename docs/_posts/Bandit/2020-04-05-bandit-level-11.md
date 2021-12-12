---
layout: post
title: "OverTheWire: Bandit Level 11"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 11 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 11 of Bandit from OverTheWire Wargames.

We found the password from [level 10](bandit-level-10).

Username: `bandit11`  
Password: `IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`

The information tells us we need to rotate the text in `data.txt` by 13 positions. Commonly known as a rot13 cipher.

So let's open up a shell using SSH and `cat data.txt`.

![](/assets/posts/OverTheWire/Bandit/Bandit11/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit11/picture2.png)

This is another level which can be cleared by googling rot13 cipher and pasting in the line of text. This is also a tricky thing to do in bash as there is no function that can magically rotate letters.

There is a function though that can translate letters call `tr`. Our purpose of using this command is to translate our line of text by 13 places, half the alphabet.  
To do this is a bit tricky and requires you know a little bit of regular expressions.  
(This here is a good little exercise which introduces gently regular expressions [https://regexone.com/](https://regexone.com/))

First we need to list all the current characters in use with `a-zA-Z`.  
And to rotate by 13, we need to then specify an out of order alphabet by 13 characters. `n-za-mN-ZA-M`  
Given in command form:

![](/assets/posts/OverTheWire/Bandit/Bandit11/picture3.png)

Which gives the password to the next level.

To continue, please read my Bandit 12 walkthrough. {% include elements/button.html link="bandit-level-12" text="Level 12" %}

Thank you for reading. :+1: