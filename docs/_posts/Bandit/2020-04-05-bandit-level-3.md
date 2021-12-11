---
layout: post
title: "OverTheWire: Bandit Level 3"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 3 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 3 of Bandit from OverTheWire Wargames.

We found the password from [level 2](bandit-level-2).

Username: `bandit3`  
Password: `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`

First we SSH into the box.

![](/assets/posts/OverTheWire/Bandit/Bandit3/picture1.png)

We then list the files in the home directory.

![](/assets/posts/OverTheWire/Bandit/Bandit3/picture2.png)

We then see a directory called `inhere`.  
Let's change the directory and list the files.

![](/assets/posts/OverTheWire/Bandit/Bandit3/picture3.png)

But there is nothing in this directory.
Another option that can be added to `ls` is `-a`. This option allows `ls` to read file that would be otherwise hidden.

![](/assets/posts/OverTheWire/Bandit/Bandit3/picture4.png)

Notice now that there are 2 directories and a file. I won't get into too much detail into what each directory means.  
But the "." directory points to the current directory. So if we were to `cd` into this directory we wouldn’t move anywhere.  
The ".." directory points to the directory above the current directory. So by `cd`-ing into that directory, would move us into the previous directory.  
We can `cat` files that have a dot point in front of its name just like any file and doing so reveals the password to the next level.

![](/assets/posts/OverTheWire/Bandit/Bandit3/picture5.png)

To continue, please read my Bandit 4 walkthrough. {% include elements/button.html link="bandit-level-4" text="Level 4" %}

Thank you for reading. :+1: