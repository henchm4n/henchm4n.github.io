---
layout: post
title: "OverTheWire: Leviathan Level 5"
tags: [OverTheWire, Leviathan]
style: fill
comments: true
color: danger
description: Walkthrough of Level 5 of OverTheWire Leviathan
---

This is going to be a walkthrough of the 5th level of OverTheWire's wargame Leviathan. So let's SSH into the machine to get started. If you haven't gotten the password, you can read my walkthrough of the [last level](leviathan-level-4).

Username: `leviathan4`  
Password: `vuH0coox6m`

![](/assets/posts/OverTheWire/Leviathan/Level5/picture1.png)

When we list the files in the home directory, we need to use the `-`a flag to list hidden files as there is a hidden directory in the home folder. 

![](/assets/posts/OverTheWire/Leviathan/Level5/picture2.png)

So we can navigate to that home directory and list out the files in that directory.

![](/assets/posts/OverTheWire/Leviathan/Level5/picture3.png)

All we get is another executable file called **bin**. Which we can run and see what information it outputs.

![](/assets/posts/OverTheWire/Leviathan/Level5/picture4.png)

And we get a list of binary values. What we can do with these values, is convert them to decimal to see if there is any information new can get out of them.

![](/assets/posts/OverTheWire/Leviathan/Level5/picture5.png)

And so we get a list of decimal values around the 100 mark. This looks oddly close to the letters in the ascii table and so we can now look up each of the decimal values for its corresponding value in ASCII. [http://www.asciitable.com/](http://www.asciitable.com/)
We get the following string, `Tith4cokei`, which is the password for the next level.

To continue, please read my Leviathan 6 walkthrough. {% include elements/button.html link="leviathan-level-6" text="Level 6" %}

Thank you for reading. :+1: