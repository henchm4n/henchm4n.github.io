---
layout: post
title: "OverTheWire: Bandit Level 15"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 15 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 15 of Bandit from OverTheWire Wargames.

We found the password from [level 14](bandit-level-14).

Username: `bandit15`  
Password: `BfMYroe26WYalil77FoDi9qh59eK5xNr`

Looking at the website, we see that we have to connect to another port on localhost but this time we have to use SSL encryption.  
Lets SSH into the machine and get started.

![](/assets/posts/OverTheWire/Bandit/Bandit15/picture1.png)

To connect to port `30001`, we can't use the same tool as last time as we need to connect with SSL encryption. So we will use the `openssl`
 command.  
Reading the first page of the second helpful resource actually shows us which command we need to use in order to connect to a particular port. But here is the description of the command we will be using.

![](/assets/posts/OverTheWire/Bandit/Bandit15/picture2.png)

So the command in this case will be

![](/assets/posts/OverTheWire/Bandit/Bandit15/picture3.png)

In which we have to enter in this levels password to return the next levels password.

![](/assets/posts/OverTheWire/Bandit/Bandit15/picture4.png)

To continue, please read my Bandit 16 walkthrough. {% include elements/button.html link="bandit-level-16" text="Level 16" %}

Thank you for reading. :+1: