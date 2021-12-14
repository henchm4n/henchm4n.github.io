---
layout: post
title: "OverTheWire: Bandit Level 4"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 4 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 4 of Bandit from OverTheWire Wargames.

We found the password from [level 3](bandit-level-3).

Username: `bandit4`  
Password: `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`

Remember to always check out the information given on the OverTheWire website about the level. It gives good clues on how to solve the level including commands you may need and sometimes some helpful reading material

So to start, we SSH into the box and list what's in the directory.

![](/assets/posts/OverTheWire/Bandit/Bandit4/picture1.png)

![](/assets/posts/OverTheWire/Bandit/Bandit4/picture2.png)

Notice there is more information now showing in the home directory. Do a google on what each "." file means. But they are normal files to have and we can ignore them.

Changing directories into the `inhere` directory and listing the files gives us a list of 10 files.

![](/assets/posts/OverTheWire/Bandit/Bandit4/picture3.png)

An easy way to solve this level is to just `cat` each file and remember to use the prefix in from of the - so `cat` knows it is a file.  
But the way to solve this level properly is by using the `file` command.  
The `file` command is used to determine the file type of a particular file.  

So if we used the `file` command on `-file00`

![](/assets/posts/OverTheWire/Bandit/Bandit4/picture4.png)

It shows that the file just contains data.  
We can then use the `file` command on all the files to see which one contains text.  
A shortcut is to use wildcards. (Link to information: [http://www.robelle.com/smugbook/wildcard.html](http://www.robelle.com/smugbook/wildcard.html))  

By making use of the "*" wildcard, we can search all the files at once.

![](/assets/posts/OverTheWire/Bandit/Bandit4/picture5.png)

As we can see, `-file07` is the only file that contains text. `cat`-ting the file gives us the next password.

![](/assets/posts/OverTheWire/Bandit/Bandit4/picture6.png)

To continue, please read my Bandit 5 walkthrough. {% include elements/button.html link="bandit-level-5" text="Level 5" %}

Thank you for reading. :+1: