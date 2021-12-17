---
layout: post
title: "OverTheWire: Leviathan Level 3"
tags: [OverTheWire, Leviathan]
style: fill
comments: true
color: danger
description: Walkthrough of Level 3 of OverTheWire Leviathan
---

We can get started with the third level of Leviathan by connecting to the remote machine with SSH. If you haven't gotten the password, you can read my walkthrough of the [last level](leviathan-level-2).

Username: `leviathan2`  
Password: `ougahZi8Ta`

![](/assets/posts/OverTheWire/Leviathan/Level3/picture1.png)

When we use the `ls` command to list all the files in the home directory.

![](/assets/posts/OverTheWire/Leviathan/Level3/picture2.png)

We see there is another executable file that we can run. So let's do just that.

![](/assets/posts/OverTheWire/Leviathan/Level3/picture3.png)

And the file has given us a usage message, telling us that we need to run the executable with a filename as an argument. We notice that in the `ls` command, it gives us the name of the user who owns the file as **leviathan3**. So we can try and aim the executable at the leviathan3 password file to see if it will print out the next levels password. 

![](/assets/posts/OverTheWire/Leviathan/Level3/picture4.png)

And it says that we don't have access to that file. So we need to come up with a solution that will enable us to print out the password in the password file.  
To do this, we need to use a very clever trick with the link command and escape characters.  
Firstly, we need to create a new directory in the `tmp/` folder and create a file that contains a space in its filename.

![](/assets/posts/OverTheWire/Leviathan/Level3/picture5.png)

And now what we can do, is use the `ln` command, which can be used to create links between files. If you haven't heard of this before, here is an article you can read which talks through links. [https://www.linux.com/topic/desktop/understanding-linux-links/](https://www.linux.com/topic/desktop/understanding-linux-links/)

The type of link we want to create is a symbolic link, but we are only going to link it to a non-existent file called **pass**. This is so when we run the `printfile` command, it will first check and print out the symbolic link file, before checking to see if it exists since we are entering in a valid filename.
So that will look like the following.

![](/assets/posts/OverTheWire/Leviathan/Level3/picture6.png)

So it prints out the password of the symbolic link before actually checking if the file exists as we didn't create a file called **pass**.  
So the next levels password is `Ahdiemoo1j`

To continue, please read my Leviathan 4 walkthrough. {% include elements/button.html link="leviathan-level-4" text="Level 4" %}

Thank you for reading. :+1: