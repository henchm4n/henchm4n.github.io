---
layout: post
title: "OverTheWire: Bandit Level 28"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 28 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 28 of Bandit from OverTheWire Wargames.

We found the password from [level 27](bandit-level-27).

Username: `bandit28`  
Password: `0ef186ac70e04ea33b4c1853d2526fa2`

We start this level by logging onto the box and by creating a new directory in `/tmp`. Then we can use the same method as last level and clone in the git repository.

![](/assets/posts/OverTheWire/Bandit/Bandit28/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit28/picture2.png)

Navigating to the `README.md` file.

![](/assets/posts/OverTheWire/Bandit/Bandit28/picture3.png)

We see that it contains information on the password but it has been blanked out. So to do some investigating with git, we can look at the history and see what the previous commits have been.

![](/assets/posts/OverTheWire/Bandit/Bandit28/picture4.png)

And we notice that one of the commits is the initial commit and then fixing the information link, so we want to revert our repository back to one of the previous commits. We can do that with the `checkout` command.

![](/assets/posts/OverTheWire/Bandit/Bandit28/picture5.png)

Now when we check the contents of the `README.md` file. It contains the password to the next level.

![](/assets/posts/OverTheWire/Bandit/Bandit28/picture6.png)

To continue, please read my Bandit 29 walkthrough. {% include elements/button.html link="bandit-level-29" text="Level 29" %}

Thank you for reading. :+1: