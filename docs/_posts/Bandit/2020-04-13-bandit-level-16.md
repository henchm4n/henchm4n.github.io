---
layout: post
title: "OverTheWire: Bandit Level 16"
tags: [OverTheWire, Bandit]
style: fill
comments: true
color: success
description: Walkthrough of Level 16 of OverTheWire Bandit
---

This is going to be a walkthrough of Level 16 of Bandit from OverTheWire Wargames.

We found the password from [level 15](bandit-level-15).

Username: `bandit16`  
Password: `cluFn7wTiGryunymYOu4RcffSxQluehd`

The information on the website tells us that there is a port between `31000` and `32000` that is listening for connections but only one of them will speak SSL.

So to start, lets connect to the level.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture1.png)

First we need to do a scan of all the ports between `31000` and `32000`. We can do that with `nmap`, a port scanning tool. We need to specify which ports and scan localhost.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture2.png)
![](/assets/posts/OverTheWire/Bandit/Bandit16/picture3.png)

As we can see, `nmap` found 2 ports but doesn't know what service they are running. We can add another option which probes to check the service info.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture4.png)

This scan does take some time to complete so be patient.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture5.png)

We see that that port `31790` is running on SSL so now we can use `openssl` to connect to that port and submit our current password.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture6.png)
![](/assets/posts/OverTheWire/Bandit/Bandit16/picture7.png)

This time however, instead of receiving the next levels password, we receive a private key for the next level.
```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```
There are two ways we can now proceed. We can copy this file this file into a file in `/tmp` and use the same method as level 13 using `ssh`. Or we can copy the file onto our own computer and connect using `ssh`.
I am going to copy the file into a folder in `/tmp` and submit the key to get access to bandit 17.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture8.png)

Make sure you change the permission on the SSH key file or else it won't work. If you do try and use the SSH key file, it will give you an error message warning you of a unprotected private key.  
That is because a private key needs to have read access to only the user or group but not everyone. So we need to run `chmod 600` on the SSH key file.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture9.png)

And we have access to bandit 17 and can obtain the password.

![](/assets/posts/OverTheWire/Bandit/Bandit16/picture10.png)

To continue, please read my Bandit 17 walkthrough. {% include elements/button.html link="bandit-level-17" text="Level 17" %}

Thank you for reading. :+1: