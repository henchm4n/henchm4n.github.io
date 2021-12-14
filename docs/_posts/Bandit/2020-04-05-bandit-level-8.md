---
layout: post
title: "OverTheWire: Bandit Level 8"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 8 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 8 of Bandit from OverTheWire Wargames.

We found the password from [level 7](bandit-level-7).

Username: `bandit8`  
Password: `cvX2JJa4CFALtqS87jk27qwqGhBM9plV`

This level is asking us to use pipes in order to separate information from a file.

First we SSH into the box and list all the files.

![](/assets/posts/OverTheWire/Bandit/Bandit8/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit8/picture2.png)

So the password is somewhere in `data.txt` and when we have a look at what `data.txt` contains, we see that it is full of possible passwords.

![](/assets/posts/OverTheWire/Bandit/Bandit8/picture3.png)
![](/assets/posts/OverTheWire/Bandit/Bandit8/picture4.png)

The information about the level tells us that the password will only appear once in the file. So we need to use commands that pull out the only unique line in `data.txt`.  
To do this, we need to use pipes. Some information about pipes is given in the Helpful reading material if you are not too familiar with pipes.

The commands we are going to use are `sort` and `uniq`. The `sort` command does exactly as it sounds, sorts the file in alphabetical order. The reason we are using `sort` is because `uniq` only gets rid of duplicate files if they are next to each other.

Firstly we need to `cat` the file onto the screen.

![](/assets/posts/OverTheWire/Bandit/Bandit8/picture5.png)

Then we can use a pipe to the `sort` command to sort the output in alphabetical order.

![](/assets/posts/OverTheWire/Bandit/Bandit8/picture6.png)

Once this is done, we can then pipe it to the `uniq` command with a certain flag set.

![](/assets/posts/OverTheWire/Bandit/Bandit8/picture7.png)
![](/assets/posts/OverTheWire/Bandit/Bandit8/picture8.png)

And that gives us the password to the next level.

To continue, please read my Bandit 9 walkthrough. {% include elements/button.html link="bandit-level-9" text="Level 9" %}

Thank you for reading. :+1: