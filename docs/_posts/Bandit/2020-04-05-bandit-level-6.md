---
layout: post
title: "OverTheWire: Bandit Level 6"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 6 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 6 of Bandit from OverTheWire Wargames.

We found the password from [level 5](bandit-level-5).

Username: `bandit6`  
Password: `DXjZPULLxYr17uwoI01bNLQbtFemEgo7`

The information given to us this time on the website is that the next password is stored somewhere on the server that is owned by user `bandit7`, owned by group `bandit6` and is 33 bytes in size.

So when we SSH into the box, we see that our home directory is empty.

![](/assets/posts/OverTheWire/Bandit/Bandit6/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit6/picture2.png)

So we will be using the `find` command again but instead of searching in the current directory, we will be searching the whole system.

1: 33 bytes in size.
This is the same flag as used in the previous exercise.

![](/assets/posts/OverTheWire/Bandit/Bandit6/picture3.png)

Because we are searching through the entire system, we are bound to encounter some errors. Because we don't want them in our output, we can use a bash trick to redirect all errors to a file to make the not appear on our screen. 

![](/assets/posts/OverTheWire/Bandit/Bandit6/picture4.png)

This is called file redirection and here is a link to some information about that: [https://www.tldp.org/LDP/abs/html/io-redirection.html](https://www.tldp.org/LDP/abs/html/io-redirection.html)
`/dev/null` is a file that is constantly being filled by the system with random information and so we can also pipe in information to that file, knowing it will be lost.

2 & 3: Owned by group `bandit6` and owned by user `bandit7`
There are options in find that allows files to be searched by the group they belong to and the user that owns them.

![](/assets/posts/OverTheWire/Bandit/Bandit6/picture5.png)
![](/assets/posts/OverTheWire/Bandit/Bandit6/picture6.png)

So we can search for group `bandit6` and user `bandit7`.

![](/assets/posts/OverTheWire/Bandit/Bandit6/picture7.png)

Putting it all together.

![](/assets/posts/OverTheWire/Bandit/Bandit6/picture8.png)

We find only one file which is the one that contains the next levels password.

![](/assets/posts/OverTheWire/Bandit/Bandit6/picture9.png)

To continue, please read my Bandit 7 walkthrough. {% include elements/button.html link="bandit-level-7" text="Level 7" %}

Thank you for reading. :+1: