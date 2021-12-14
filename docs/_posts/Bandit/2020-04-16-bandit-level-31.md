---
layout: post
title: "OverTheWire: Bandit Level 31"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 31 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 31 of Bandit from OverTheWire Wargames.

We found the password from [level 30](bandit-level-30).

Username: `bandit31`  
Password: `47e603bb428404d265f59c42920d81e5`

First we can start the level like the previous ones by connecting to the level, creating a directory in `/tmp/` and cloning the repository.

![](/assets/posts/OverTheWire/Bandit/Bandit31/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit31/picture2.png)

We can see that there are instructions in the `README` file that specify that we need to push a file into the remote repository. The first trick we have to do is to remove the `.gitignore`.

![](/assets/posts/OverTheWire/Bandit/Bandit31/picture3.png)

Now we can create a file called `key.txt` that contains the details provided.

![](/assets/posts/OverTheWire/Bandit/Bandit31/picture4.png)

We do a check to make sure the file was created successfully.  
Now we can upload the file using the following git commands.  
First we add the file, then we commit it with a message, then we push the file to the correct branch of master.

![](/assets/posts/OverTheWire/Bandit/Bandit31/picture5.png)

And we get the password to the next level.

To continue, please read my Bandit 32 walkthrough. {% include elements/button.html link="bandit-level-32" text="Level 32" %}

Thank you for reading. :+1: