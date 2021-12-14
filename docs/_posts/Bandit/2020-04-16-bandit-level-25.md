---
layout: post
title: "OverTheWire: Bandit Level 25"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 25 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 25 of Bandit from OverTheWire Wargames.

We found the password from [level 24](bandit-level-24).

Username: `bandit25`  
Password: `uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG`

The information on the website tells us that the shell for bandit26 is not `/bin/bash` so we need to find out what it is.  
So lets start by SSH-ing into the level.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit25/picture2.png)

As we can now see, we have been given bandit26's ssh key which we should be able to use to log into bandit26.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture3.png)
![](/assets/posts/OverTheWire/Bandit/Bandit25/picture4.png)

But when we try and login to bandit26, our connection is closed. The information on the website said that bandit26's shell was not `/bin/bash` so we now need to go and check what it's shell is.  
We can do that by checking the **passwd** file as there is a column that specifies the logon shell.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture5.png)
![](/assets/posts/OverTheWire/Bandit/Bandit25/picture6.png)

We can see that bandit26 does indeed login with a different shell. So let's see what information the **showtext** file has.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture7.png)  

So when we log into bandit26, we are shown a the text file located in bandit26s home directory and then are forced to exit.  
A way to get around this is using a vulnerability in the `more` command. The way to do this is to make the terminal window as small as possible so that more activates and shows you its interface.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture8.png)
![](/assets/posts/OverTheWire/Bandit/Bandit25/picture9.png)

Once you are in this view, you can press 'v' which then opens the file into `vim`, which we have much more control of.  
We can also rescale our window again.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture10.png)

There are 2 things we can now do. In `vim`, we can see the contents of a new file by opening it. The command to do that is with `e`.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture11.png)
![](/assets/posts/OverTheWire/Bandit/Bandit25/picture12.png)

And we get the password for the next level.  
The next thing we have to do is to pop a shell so that we can do the next level of the challenge. If we try and log into bandit26 we will fail the same way and face the same problem.
So we need to execute a command in vim that changes the shell used.

![](/assets/posts/OverTheWire/Bandit/Bandit25/picture13.png)
![](/assets/posts/OverTheWire/Bandit/Bandit25/picture14.png)
![](/assets/posts/OverTheWire/Bandit/Bandit25/picture15.png)

And now we have a shell for the next level. 

To continue, please read my Bandit 26 walkthrough. {% include elements/button.html link="bandit-level-26" text="Level 26" %}

Thank you for reading. :+1: