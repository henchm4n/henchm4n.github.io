---
layout: post
title: "OverTheWire: Bandit Level 12"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 12 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 12 of Bandit from OverTheWire Wargames.

We found the password from [level 11](bandit-level-11).

Username: `bandit12`  
Password: `5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu`

The information on the website tells us that `data.txt` is a hexdump of a file that has been compressed repeatedly. And also tells us that we should create a directory in `/tmp`.

So let's start by SSH-ing into the box and try reading `data.txt`.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture1.png)  
![](/assets/posts/OverTheWire/Bandit/Bandit12/picture2.png)

As we can see, `data.txt` is a hex dump of a file. We can use the command `xxd` which allows us to reverse a hexdump.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture3.png)

But before we do that, we should make a directory in `/tmp` so that we can output the file in the current directory. So we make the directory, copy `data.txt` into the directory and `cd` into the newly created directory.  
You can call the directory anything you want, but something relating to the levels is good as you will need to create more directories as we progress along the levels.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture4.png)

Now lets use `xxd` to revert the hexdump, specifying an output file.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture5.png)

Now when we try and `cat` the file, we get.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture6.png)

Nothing.  
This is because the file was also compressed multiple times and so `cat` cannot output the file in a nice format. To specify which format the file is in, we use the `file` command.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture7.png)

So now we need to de-compress the data which has been compressed with gzip. There are 2 ways we can do this. Using the `gunzip` command or using `gzip` with `-d` for de-compress.  
We will be using `gunzip` and need to specify the suffix of the file since it is not the `.gz` default that gzip supports.  
There is also no need to specify an output file as gunzip will modify file.txt to be uncompressed.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture8.png)

We can now use the `file` command on the file to see what type of file it is.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture9.png)

Now we see that the file is compressed with another compressor, namely bzip2. So lets go ahead and use `bunzip2`, which is bzip2's de-compression command, to decompress the file.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture10.png)

Again we see that it is compressed with gzip. We can continue this process until we reach a file that is not compressed.

![](/assets/posts/OverTheWire/Bandit/Bandit12/picture11.png)

As we can now see, we eventually end up with an ASCII text file that contains the next levels password.

To continue, please read my Bandit 13 walkthrough. {% include elements/button.html link="bandit-level-13" text="Level 13" %}

Thank you for reading. :+1: