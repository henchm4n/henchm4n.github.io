---
layout: post
title: "OverTheWire: Bandit Level 20"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 20 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 20 of Bandit from OverTheWire Wargames.

We found the password from [level 19](bandit-level-19).

Username: `bandit20`  
Password: `GbKksEFF4yrVs6il55v6gwY5aVje5f0j`

The information given on the website tells us that the binary file connects to a port, reads a line of text and if it matches this levels password, it will give us the password to the next level.

So lets start SSH and have a look at the binary.

![](/assets/posts/OverTheWire/Bandit/Bandit20/picture1.png)  
![](/assets/posts/OverTheWire/Bandit/Bandit20/picture2.png)

As we can see, we need to somehow specify a port that we can input the next levels password. To do that, we will be using `nc` and `tmux`.

 We have already used `nc` but only connecting to another port and not listening on one. To do this, we need to specify the `-l` flag which listen's for inbound connections.

![](/assets/posts/OverTheWire/Bandit/Bandit20/picture3.png)

Tmux is going to be used to open 2 bash sessions side by side which will let us use the same connection without having to ssh in from another terminal. Here is an introductory guide to tmux: [https://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/](https://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/)

So we start by creating a new tmux session and splitting the screen by pressing CTRL-%

![](/assets/posts/OverTheWire/Bandit/Bandit20/picture4.png)  
![](/assets/posts/OverTheWire/Bandit/Bandit20/picture5.png)

And as you can see, we now have a split screen with 2 terminals. We can move across to the right terminal by typing `CTRL-b` "<right arrow>". Now we can set up our `nc` session. Also using the `-p` flag so we can choose our own port.

![](/assets/posts/OverTheWire/Bandit/Bandit20/picture6.png)

Move over to the left window and we are going to use the binary and specify the port number of our listener.

![](/assets/posts/OverTheWire/Bandit/Bandit20/picture7.png)

Once we have done that, we move back into the right pane and enter in this levels password.

![](/assets/posts/OverTheWire/Bandit/Bandit20/picture8.png)

And as you can see, when we submit the password, the binary recognises that the password is correct and sends the next levels password.

To continue, please read my Bandit 21 walkthrough. {% include elements/button.html link="bandit-level-21" text="Level 21" %}

Thank you for reading. :+1: