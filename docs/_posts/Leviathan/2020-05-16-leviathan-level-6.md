---
layout: post
title: "OverTheWire: Leviathan Level 6"
tags: [OverTheWire, Leviathan]
style: fill
comments: true
color: danger
description: Walkthrough of Level 6 of OverTheWire Leviathan
---

This is a walkthrough of the 6th level of OverTheWire's wargame Leviathan. As with previous levels, we can SSH into the remote machine to get started. If you haven't gotten the password, you can read my walkthrough of the [last level](leviathan-level-5).

Username: `leviathan5`  
Password: `Tith4cokei`

![](/assets/posts/OverTheWire/Leviathan/Level6/picture1.png)

When we list the files in the home directory.

![](/assets/posts/OverTheWire/Leviathan/Level6/picture2.png)

There is an executable file called **leviathan5**. So let's run the file and see what information it prints out for us.

![](/assets/posts/OverTheWire/Leviathan/Level6/picture3.png)

It looks like it is trying to access a file called **file.log** in the `tmp` directory. So let's create a file called **file.log** and see what it does once its created. I am going to put the echo command in the file just to see if the executable will do anything with the contents of the file.

![](/assets/posts/OverTheWire/Leviathan/Level6/picture4.png)

We see that the executable file has printed out the contents of the **file.log** file. So we can use the linking trick we learnt from earlier to link the `leviathan6` password file to the **file.log** file.

![](/assets/posts/OverTheWire/Leviathan/Level6/picture5.png)

And we see that the password for the next level is `UgaoFee4li`.

To continue, please read my Leviathan 7 walkthrough. {% include elements/button.html link="leviathan-level-7" text="Level 7" %}

Thank you for reading. :+1: