---
layout: post
title: "OverTheWire: Bandit Level 13"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 13 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 13 of Bandit from OverTheWire Wargames.

We found the password from [level 12](bandit-level-12).

Username: `bandit13`  
Password: `8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL`

The information on the website says that we are looking for a private SSH key, needed to log on to the next level.  
So lets start by SSH-ing into the box and looking around to see what we can see.

![](/assets/posts/OverTheWire/Bandit/Bandit13/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit13/picture2.png)

We see a file called `sshkey.private`. Upon inspection, we see that the file is in fact a private key.

![](/assets/posts/OverTheWire/Bandit/Bandit13/picture3.png)

So this must be the private key that the website was referring too.  
There is a parameter in SSH which you can specify a private key. This is so ssh uses the private key instead of using a password.

![](/assets/posts/OverTheWire/Bandit/Bandit13/picture4.png)

We also don't need to end the connection to move onto the next level as we can SSH straight from `bandit13`. Instead of using `bandit.labs.overthewire.org`, we can just write `localhost`, which is what the computer to specify the current hostname.

![](/assets/posts/OverTheWire/Bandit/Bandit13/picture5.png)

And we are in.  
For future reference, we can `cat /etc/bandit_pass/bandit14` to obtain the password for future use.

![](/assets/posts/OverTheWire/Bandit/Bandit13/picture6.png)

To continue, please read my Bandit 14 walkthrough. {% include elements/button.html link="bandit-level-14" text="Level 14" %}

Thank you for reading. :+1: