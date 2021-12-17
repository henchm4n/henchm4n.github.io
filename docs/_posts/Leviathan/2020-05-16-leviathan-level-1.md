---
layout: post
title: "OverTheWire: Leviathan Level 1"
tags: [OverTheWire, Leviathan]
style: fill
comments: true
color: danger
description: Walkthrough of Level 1 of OverTheWire Leviathan
---

This series of posts will be a walkthrough of the Leviathan challenges on OverTheWire which focus on basic Linux commands. Each level doesn't have any information about them on the website so we have to work out what to do, based on what we see when we log into the level on the remote host.

So let's get started with the first level by logging into the remote machine using the path `leviathan.labs.overthewire.org` and on port `2223`.

Username: `leviathan0`  
Password: `leviathan0`

![](/assets/posts/OverTheWire/Leviathan/Level1/picture1.png)

The first command we can run is the `ls -al` command which searches the current directory for all files, including hidden ones.

![](/assets/posts/OverTheWire/Leviathan/Level1/picture2.png)

And we encounter a directory called `.backup`. So we can enter into the directory using `cd`, and use the list command again to list all possible directories and files.

![](/assets/posts/OverTheWire/Leviathan/Level1/picture3.png)

There is a html file called **bookmarks.html** which we can have a look at with the `cat` command. This will put the contents of the file onto the terminal so we can read it.

![](/assets/posts/OverTheWire/Leviathan/Level1/picture4.png)

But, we get a long output with a lot of irrelevant text. This is of course, not useful for us as we are looking for the password to the next level. So we can pipe this output to the `grep` command and search for any strings which contain the word password. With html files, passwords are usually found next to a comment called pass or password to let the creator of the file know, what the string is. 

So with the `grep` command, we get the following output. 

![](/assets/posts/OverTheWire/Leviathan/Level1/picture5.png)

Which lets us know that the next levels password is `rioGegei8m`.

To continue, please read my Leviathan 2 walkthrough. {% include elements/button.html link="leviathan-level-2" text="Level 2" %}

Thank you for reading. :+1: