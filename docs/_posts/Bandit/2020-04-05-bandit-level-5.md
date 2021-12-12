---
layout: post
title: "OverTheWire: Bandit Level 5"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 5 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 5 of Bandit from OverTheWire Wargames.

We found the password from [level 4](bandit-level-4).

Username: `bandit5`  
Password: `koReBOKuIDDepwhWk7jZC0RTdopnAYKh`

The information on the webpage tells us that we are looking for a file that is human-readable, 1033 bytes in size and is not executable.

First we SSH into the box and list the files in the home directory.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture1.png)

We are again given a directory called `inhere`.  
Changing the directory to it and listing all the files gives a list of directories.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture2.png)

Looking into one of these directories gives us a list of files. We can use `ls` without changing the directory by giving it a path to the directory.  
In this case, the path is just the directory name. But we could of also typed `ls -al ~/inhere/maybehere10` and that would of given us the same result.  

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture3.png)

Each of these files contains a different number of bytes of which none are 1033 bytes in size.  
But because there are multiple directories, we can't use the same trick as last time.  
The command we will be using this time is the `find` command. This command searches for files through directories given search parameters. Here is a link which gives an introduction to commands: [https://www.linode.com/docs/tools-reference/tools/find-files-in-linux-using-the-command-line/](https://www.linode.com/docs/tools-reference/tools/find-files-in-linux-using-the-command-line/)

So we need to use the `find` command to search for 3 things.

1: 1033 bytes in size.  
This can be accomplished with the flag `-size` and the suffix of `c` as can be seen in the man page.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture4.png)

So using this command with `find` gives us the following output.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture5.png)

When we `cat` this file it gives us the next password.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture6.png)

You can stop here but if you're interested then I'm going to show how you can use find to search for the other properties.

2: Not executable.  
There is a flag in `find` that checks whether a file is executable.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture7.png)

The problem is that it returns files that are only executable when we want the opposite. We can do this by putting a "!" in front of the flag. The "!" symbol is used by bash to symbolise "NOT", a binary expression, meaning to return everything that is not matched by a particular expression. So in our case, this means that it matches with files that are not executable. 

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture8.png)

3: Human readable.  
This one is hard to execute as its difficult to dictate what makes a file readable. In this case, we are going to consider that text files are readable. To do this, we can use a flag that executes a command and the command we are executing is the file command.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture9.png)

But the file command doesn't sort through which files are readable or not, it only prints out the type of each file. So we can use pipes to send the output to grep which we can use to search for text files.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture10.png)

Finally, we can put it all together in one command to search for the file we need.

![](/assets/posts/OverTheWire/Bandit/Bandit5/picture11.png)

To continue, please read my Bandit 6 walkthrough. {% include elements/button.html link="bandit-level-6" text="Level 6" %}

Thank you for reading. :+1: