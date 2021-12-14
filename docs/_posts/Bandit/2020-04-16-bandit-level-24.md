---
layout: post
title: "OverTheWire: Bandit Level 24"
tags: [OverTheWire, Bandit]
style: fill
color: success
description: Walkthrough of Level 24 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 24 of Bandit from OverTheWire Wargames.

We found the password from [level 23](bandit-level-23).

Username: `bandit24`  
Password: `UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ`

The website tells us that we need to connect to port `30002` and give the current password as well as a 4 digit code which we need to brute-force.  
So lets SSH into the level and start.

![](/assets/posts/OverTheWire/Bandit/Bandit24/picture1.png)
![](/assets/posts/OverTheWire/Bandit/Bandit24/picture2.png)

Now we are in the machine we need a way to brute-force all the number combinations. We can do this by creating a script that lists all the numbers and the way I am going to do it, is to create a script that adds the password in front of all the numbers so that it is already in the format we need to submit to the required port.

![](/assets/posts/OverTheWire/Bandit/Bandit24/picture3.png)
![](/assets/posts/OverTheWire/Bandit/Bandit24/picture4.png)

So the script goes through each number from 0000 - 9999, with the `-w` keeping all the 0's there and not disappearing, and puts the password in front of the number.  
When we execute the script, making sure to use `chmod` to make the script executable, we get a long list of passwords and numbers.

![](/assets/posts/OverTheWire/Bandit/Bandit24/picture5.png)

What we can do now, is pipe this script to `nc` on port `30002`. I am also going to redirect the output to a file so that it is easier to read. This will take a minute due to the large amount of queries being sent.

![](/assets/posts/OverTheWire/Bandit/Bandit24/picture6.png)

It seems though we have encountered a timeout error as our command was too long. But we can search through what we have to see if we have encountered the password. The way I am going to do this is with `grep` using the `-Ev` options which match the inverse of what we are searching. 

![](/assets/posts/OverTheWire/Bandit/Bandit24/picture7.png)

And we see that we have yet to find our password. So now we can go into our script and change the start number to something higher so that the command has less numbers to search through.

![](/assets/posts/OverTheWire/Bandit/Bandit24/picture8.png)

I have changed the numbers 0000 to 7300. Now lets run the same command again but specify a different output file.

![](/assets/posts/OverTheWire/Bandit/Bandit24/picture9.png)

As we can see, the script executed and exited, giving us the password to the next level. The `tail` command letting us see the last 10 lines of a file.

To continue, please read my Bandit 25 walkthrough. {% include elements/button.html link="bandit-level-25" text="Level 25" %}

Thank you for reading. :+1: