---
layout: post
title: "OverTheWire: Leviathan Level 4"
tags: [OverTheWire, Leviathan]
style: fill
comments: true
color: danger
description: Walkthrough of Level 4 of OverTheWire Leviathan
---

This is going to be a walkthrough of the 4th level of the Leviathan OverTheWire wargame and so to begin, we need to SSH into the remote host. If you haven't gotten the password, you can read my walkthrough of the [last level](leviathan-level-3).

Username: `leviathan3`  
Password: `Ahdiemoo1j`

![](/assets/posts/OverTheWire/Leviathan/Level4/picture1.png)

Doing a list of the files in the home directory. 

![](/assets/posts/OverTheWire/Leviathan/Level4/picture2.png)

We see an executable file called **level3**. So let's run the file and see if it gives us any usage information.

![](/assets/posts/OverTheWire/Leviathan/Level4/picture3.png)

It doesn't give us any information but asks us to enter in a password. I am just going to type in password and see what other information it prints out.

![](/assets/posts/OverTheWire/Leviathan/Level4/picture4.png)

And it let's us know that we entered in the wrong password. We can use the same trick as the Level 2 by using the `ltrace` command to see if it executes any commands we can see. I am going to be typing in the same password as my password.

![](/assets/posts/OverTheWire/Leviathan/Level4/picture5.png)

We see that it compares a couple of strings before asking us what our password is. Then it compares what we entered with the string `snlprintf` before letting us know that our password was wrong. So let's try the command again with `snlprintf` as our password and see what happens.

![](/assets/posts/OverTheWire/Leviathan/Level4/picture6.png)

And it appears that it worked and we have obtained a shell on the machine as the `leviathan4` user. So we can open the password file in the password folder which gives us `vuH0coox6mas` the password for the next level.

To continue, please read my Leviathan 5 walkthrough. {% include elements/button.html link="leviathan-level-5" text="Level 5" %}

Thank you for reading. :+1: