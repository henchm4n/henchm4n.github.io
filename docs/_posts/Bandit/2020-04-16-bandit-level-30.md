---
layout: post
title: "OverTheWire: Bandit Level 30"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 30 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 30 of Bandit from OverTheWire Wargames.

We found the password from [level 29](bandit-level-29).

Username: `bandit30`  
Password: `5b90576bedb2cc04c86a9e924ce42faf`

This levels starts the same as the last one by connecting to the machine, creating a new directory in `/tmp/` and cloning the git repository.

![](/assets/posts/OverTheWire/Bandit/Bandit30/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit30/picture2.png)

So we see that this time the `README.md` file doesn't give us any information. We can check the logs and the branches but they both don't contain any information. If you read the manpage,  you come across this command.

![](/assets/posts/OverTheWire/Bandit/Bandit30/picture3.png)

Git supports tags which are used to specify an important commit. So let's check if tags have been used.

![](/assets/posts/OverTheWire/Bandit/Bandit30/picture4.png)

We see indeed that there is a tag and so we can show the tag to see its information.

![](/assets/posts/OverTheWire/Bandit/Bandit30/picture5.png)

And that is the password to the next level.

To continue, please read my Bandit 31 walkthrough. {% include elements/button.html link="bandit-level-31" text="Level 31" %}

Thank you for reading. :+1: