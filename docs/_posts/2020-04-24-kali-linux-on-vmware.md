---
layout: post
title: Kali Linux on VMware Player
tags: [VMware Player, Kali]
style: fill
comments: true
color: secondary
description: Walkthrough to Install Kali Linux on VMware Player
---

Today I will be showing you how to install Kali Linux on VMware Player.

The reason we are installing Kali Linux is that it comes fully loaded with tonnes of security software and tools without us having to install it ourselves. Other security distributions are ParrotOS and BlackArch. Each of the distros is built on a different version of Linux. Kali is built atop of Ubuntu, ParrotOS on Debian and BlackArch on Arch Linux. I implore you to try each of these operating systems and see which one suits you best but I will be sticking with Kali.

There are different ways we can go about installing Kali Linux, one is with an installer image (iso) file or with an open virtualization archive format file (ova). I will be showing you how to install both with the ova installation being very easy and good for beginners but comes with limited install options that can all be changed later. The iso file is the one that I use with my Kali machine, as it's more of a fresh install then the ova installation. Feel free to skip over either section depending on which way you want to install Kali.

# Kali Linux OVA Install

To begin with, we need to head over to the downloads page and download the Kali VMware image.
[https://www.offensive-security.com/kali-linux-vm-vmware-virtualbox-image-download/](https://www.offensive-security.com/kali-linux-vm-vmware-virtualbox-image-download/)

![](/assets/posts/kali-on-vmware/picture5.png)

Once that has downloaded you should be greeted with a zip file. We now need to extract it which I'm going to put in the current directory.

![](/assets/posts/kali-on-vmware/picture6.png)
![](/assets/posts/kali-on-vmware/picture7.png)

Once that has completed you should see lots of .vmdk files in your directory.

![](/assets/posts/kali-on-vmware/picture8.png)

To install the virtual machine, we need to double click on the .vmx file.

![](/assets/posts/kali-on-vmware/picture9.png)

Which will open up a VMware Player window which will start the importing process. We can select the I Copied It option to continue.

![](/assets/posts/kali-on-vmware/picture10.png)

And we see that Kali is now installed. The default username and password is 'kali/kali' which you should change to increase your security on your machine. And that is how you install Kali Linux with a .ova file.

# Kali Linux iso Install.

To begin with the installation, we need to head over to the Kali Linux home page and download Kali Linux. We will be using the 64-bit version of Kali.
[https://www.kali.org/downloads/](https://www.kali.org/downloads/)

![](/assets/posts/kali-on-vmware/picture11.png)

Once that has finished downloading, we can start up VMware player and click on the Create a New Virtual Machine button.

![](/assets/posts/kali-on-vmware/picture12.png)

Now we need to browse to where we downloaded our virtual machine by clicking the browse button underneath the installer disc image file option.

![](/assets/posts/kali-on-vmware/picture13.png)

And we need to click open on our Kali .iso file.

![](/assets/posts/kali-on-vmware/picture14.png)

And we can click on the next button to proceed to the next step.

![](/assets/posts/kali-on-vmware/picture15.png)

We need to change the bullet point option to Linux and make sure the version is Ubuntu before clicking next to proceed.

![](/assets/posts/kali-on-vmware/picture16.png)

Now we can choose what we want to name our Virtual machine, which I will be calling it Kali Linux, and leaving the default install location as is. Now click next to proceed.

![](/assets/posts/kali-on-vmware/picture17.png)

I am going to change the disk size to 25GB and have VMware Player store my file as a single file. Click next to proceed.

![](/assets/posts/kali-on-vmware/picture18.png)

Now we do want to customise some hardware by clicking on the Customize Hardware button.

![](/assets/posts/kali-on-vmware/picture19.png)

First I am going to change the amount of RAM used to 4GB instead of 2.

![](/assets/posts/kali-on-vmware/picture20.png)

Next I am going to change the number of processors used to 2, just to make the virtual machine run faster.

![](/assets/posts/kali-on-vmware/picture21.png)

Now we can click on the Close button and click Finish to finish the VMware installation options.

![](/assets/posts/kali-on-vmware/picture23.png)

Now we can power on our machine by double clicking it, or clicking on the Play virtual machine button.

![](/assets/posts/kali-on-vmware/picture24.png)

And we are done installing Kali Linux on VMWare player 2 different ways and Metasploit.

Thank you for reading. :+1: