---
layout: post
title: "OverTheWire: Bandit Level 29"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 29 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 29 of Bandit from OverTheWire Wargames.

We found the password from [level 28](bandit-level-28).

Username: `bandit29`  
Password: `bbc96594b4e001778eee9975372716b2`

For this level, we can start by connecting to the box, create a directory in tmp and clone the git repository.

![](/assets/posts/OverTheWire/Bandit/Bandit29/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit29/picture2.png)

We are again greeted by another `README.md` file and we can open it to see what it contains.

![](/assets/posts/OverTheWire/Bandit/Bandit29/picture3.png)

It tells us that there were no passwords in production which mean that if we went through all the previous commits, we wouldn't find a password like in the last level.  
Git supports branches which allow programmers to work on their own version of the code separately from everybody else. So we can check the branches to see if they contain any information.

![](/assets/posts/OverTheWire/Bandit/Bandit29/picture4.png)

We see that there are other branches that are not the master branch. We can check in each branch to see more information about them.

![](/assets/posts/OverTheWire/Bandit/Bandit29/picture5.png)

Let's choose the `refs/heads/dev` branch and see what information it contains.

![](/assets/posts/OverTheWire/Bandit/Bandit29/picture6.png)

And we see that it contained the password to the next level.

To continue, please read my Bandit 30 walkthrough. {% include elements/button.html link="bandit-level-30" text="Level 30" %}

Thank you for reading. :+1: