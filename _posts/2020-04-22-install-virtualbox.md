---
layout: post
title: Install VirtualBox
tags: [VirtualBox]
style: fill
color: primary
description: Install VirtualBox on Windows.
---

Today I will be showing you how to install VirtualBox. VirtualBox is an open source virtualization software that makes it possible to run multiple operating systems (OS) on one computer. This virtual computer runs on top of another systems hardware using virtualization, sharing resources such as RAM, computing power and disk usage. I recommend using a computer with at least 8GB of RAM and has at least 30GB free so that we have enough space to install some virtual machines.

The reason why we are using VirtualBox is that it is a free software that runs on any modern operating system (Windows, MacOS, Linux). And it is part of the open source community, meaning that anyone can edit the software to fix bugs and security issues.

So first of all, we need to navigate to VirtualBox's downloads page and install the latest version of VirtualBox. https://www.virtualbox.org/wiki/Downloads 
Make sure you choose the right version for your host operating system. I have a windows computer and will be showing the windows VirtualBox installation. If you are not using windows you can still follow along but some settings may be different.

![](/assets/posts/install-virtualbox/virtualbox_download_page.png)

Once that has downloaded, we can start by clicking on the executable file in your Downloads folder and the setup menu is shown.

![](/assets/posts/install-virtualbox/setup_1.png)

Click next.

![](/assets/posts/install-virtualbox/setup_2.png)

You can choose to change the location where VirtualBox is installed but I will be installing it in the default location. So click next.

![](/assets/posts/install-virtualbox/setup_3.png)

Untick all of the options you don't want to be installed. I have unticked the bottom two checkboxes but you can leave defaults if that’s what you want. You can then hit the next button again.

![](/assets/posts/install-virtualbox/setup_4.png)

You don't have to worry too much about the temporary drop in network connection. It only does so to configure its network adaptor for its internal network. Click yes.

![](/assets/posts/install-virtualbox/setup_5.png)

And finally click install. A popup window will open and ask if you want to allow the program to install features. You can click yes on that one too.

![](/assets/posts/install-virtualbox/setup_6.png)

![](/assets/posts/install-virtualbox/setup_7.png)

When its finished and this screen is shown, we do want to start VirtualBox so hit finish. 

![](/assets/posts/install-virtualbox/setup_8.png)

If a popup comes up and asks to restart your computer, hit yes and do so. This will allow VirtualBox to have full functionality on your computer and setup its network drives properly.
Now we have successfully installed VirtualBox onto our computers and next, we can install some virtual machines.