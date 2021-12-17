---
layout: post
title: "OverTheWire: Leviathan Level 7"
tags: [OverTheWire, Leviathan]
style: fill
comments: true
color: danger
description: Walkthrough of Level 7 of OverTheWire Leviathan
---

This is the final level in the wargame Leviathan which has taught us commands and functions related to executables and Linux. So let's SSH into the machine and get started. If you haven't gotten the password, you can read my walkthrough of the [last level](leviathan-level-6).

Username: `leviathan6`  
Password: `UgaoFee4li`

![](/assets/posts/OverTheWire/Leviathan/Level7/picture1.png)

Listing the files in the home directory.

![](/assets/posts/OverTheWire/Leviathan/Level7/picture2.png)

We are given another binary file. So let's run the binary file and see what information it gives us.

![](/assets/posts/OverTheWire/Leviathan/Level7/picture3.png)

It tells us that when we run the binary file, we also need to supply a 4 digit code. So let's try and enter in a 4 digit code and see what it outputs.

![](/assets/posts/OverTheWire/Leviathan/Level7/picture4.png)

Okay, so it looks like we have to try and brute-force the 4 digit combination for the file. So to do this, what you can do is create a directory in in `/tmp` and write some code that executes this file with the 4 digit code incrementing. But I am just going to use the terminal to do so in a one liner using a bash for loop.

![](/assets/posts/OverTheWire/Leviathan/Level7/picture5.png)

Now this takes some time to go through all the 4 digit numbers, so be patient.

![](/assets/posts/OverTheWire/Leviathan/Level7/picture6.png)

Execution stops as it appears when we gave it the correct 4 digit code, it executed a shell for us where we are `leviathan7`. So we can go and have a look at the password file for the final password. 

![](/assets/posts/OverTheWire/Leviathan/Level7/picture7.png)

And the final password is `ahy7MaeBo9`.

For those that are interested, we can actually change the command so it also prints out the 4 digit code so we know which number was the one that was correct.

![](/assets/posts/OverTheWire/Leviathan/Level7/picture8.png)

![](/assets/posts/OverTheWire/Leviathan/Level7/picture9.png)

And the correct 4 digit value was 7123

Thank you for reading. :+1: