---
layout: post
title: "OverTheWire: Bandit Level 14"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 14 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 14 of Bandit from OverTheWire Wargames.

We found the password from [level 13](bandit-level-13).

Username: `bandit14`  
Password: `4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e`

Reading the information on the website, we can see that we need to connect to port `30000` on localhost and submit the current levels passowrd to get the password for the next level.

So lets start by SSH-ing into the maching, or if you are continuing from the previous level, you can skip this step.

![](/assets/posts/OverTheWire/Bandit/Bandit14/picture1.png)

If we do a `ls -al`, we see there are no files and that is normal. For this level, we will be using a command `nc` called netcat. This command allows us to connect or listen on particular ports on our computer to input and receive data through the connected port.

So we just need to use `nc` to connect to port `30000` on localhost and type in this levels password.

![](/assets/posts/OverTheWire/Bandit/Bandit14/picture2.png)

To continue, please read my Bandit 15 walkthrough. {% include elements/button.html link="bandit-level-15" text="Level 15" %}

Thank you for reading. :+1: