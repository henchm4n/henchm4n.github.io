---
layout: post
title: "OverTheWire: Leviathan Level 2"
tags: [OverTheWire, Leviathan]
style: fill
comments: true
color: danger
description: Walkthrough of Level 2 of OverTheWire Leviathan
---

This is going to be a walkthrough of the second level of Leviathan, an OverTheWire wargame.

First of course, we need to connect to the remote host with SSH using the credentials we got through the [last level](leviathan-level-1).

Username: `leviathan1`  
Password: `rioGegei8m`

![](/assets/posts/OverTheWire/Leviathan/Level2/picture1.png)
![](/assets/posts/OverTheWire/Leviathan/Level2/picture2.png)

When we have a look in the home directory, we come across a file called **check**, which we are allowed to execute. So let's run the command and see if it gives us any usage information.

![](/assets/posts/OverTheWire/Leviathan/Level2/picture3.png)

So the **check** binary asks us for a password, and if we enter in the right password, will do something. But first, we need to find out what the correct password is. 

We can use a command called `ltrace`, which shows us all the library calls that the binary uses such as if it needs to compare two values or needs to print out information.  
Looking at the man page for the function gives you valuable information about what a function does and how to use it.

![](/assets/posts/OverTheWire/Leviathan/Level2/picture4.png)

So when we run the function, we see that it calls the c `printf` function to print a string to the terminal, and then it halts execution as it is waiting for input from the user. So I am going to enter in password again and see what the rest of the function does. 

![](/assets/posts/OverTheWire/Leviathan/Level2/picture5.png)

We see that it calls another couple of `getchar()` functions before using the `strcmp` function. This function takes 2 string values as input and compares them to check if they are the same. It returns true if they are the same, and false otherwise. So in our case, the `strncmp` function returned false and we were greeted with a string saying we entered in the wrong password. So now we know what value the function tries and compares our value too, we can enter in that value to see if that changes things.

![](/assets/posts/OverTheWire/Leviathan/Level2/picture6.png)

And it seems that when we enter in the password as **sex**, it calls a shell on the machine. In our case, the shell didn't work because we were using the `ltrace` program to call it instead of just using the terminal. So now we know what the password is, we can go back and run the program again and enter in the correct password.

![](/assets/posts/OverTheWire/Leviathan/Level2/picture7.png)

So we obtain a shell with the `leviathan2` user and can obtain the levels password by opening the correct password file in the `/etc` folder. The next levels password is `ougahZi8Ta`.

To continue, please read my Leviathan 3 walkthrough. {% include elements/button.html link="leviathan-level-3" text="Level 3" %}

Thank you for reading. :+1: