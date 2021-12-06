---
layout: post
title: Metasploitable 2 on VirtualBox
tags: [VirtualBox, Metasploitable 2]
style: fill
color: warning
description: Walkthrough of how to install Metasploitable 2 on VirtualBox
---

Today I will be showing you how to install Metsploitable 2 on VirtualBox. 

Metasploitable 2 is a distribution vulnerable by design, and makes it easy to test out different tools and methods.

First I will show you how to download and install Metasploitable 2 as it is very easy to install. First we need to download the Metasploitable 2 files and we can do so from the following website.  [https://sourceforge.net/projects/metasploitable/](https://sourceforge.net/projects/metasploitable/)

![](/assets/posts/metasploitable-2-on-virtualbox/metasploitable_download.png)

Once the files have downloaded, we can extract the downloaded files into a directory of our choosing. I recommend 7-zip as it's free and easy to use. Once that's extracted, the files should look something like this.

![](/assets/posts/metasploitable-2-on-virtualbox/metasploitable_folder_view.png)

We can now start up VirtualBox, hit the tools menu option and select new. This will open a prompt we can follow to install a new virtual machine.

![](/assets/posts/metasploitable-2-on-virtualbox/metasploitable_open_virtualbox.png)

Your screen should now look something like this.

![](/assets/posts/metasploitable-2-on-virtualbox/metasploitable_create_vm.png)

Now we can start to fill out some of the fields. Put the name "Metasploitable 2" in the name field, you can leave the machine folder field as is. We have to change the type to Linux and the version to "Other Linux (64-bit)". Once that is set we can click next.

![](/assets/posts/metasploitable-2-on-virtualbox/metasploitable_setup_1.png)

We can leave the memory size as is as Metsaploitable 2 isn't a resource heavy virtual machine.

![](/assets/posts/metasploitable-2-on-virtualbox/metasploitable_setup_2.png)

Now we need to select to use an existing virtual hard disk file. Clicking on the folder icon.

![](/assets/posts/metasploitable-2-on-virtualbox/picture7.png)

Now we can click on the Add button and search through our operating system for the folder containing our Metasploitable 2 files.

![](/assets/posts/metasploitable-2-on-virtualbox/picture8.png)

The file we want to select should be the only file showing called Metasploitable.vmdk. Select that file and click open.

![](/assets/posts/metasploitable-2-on-virtualbox/picture9.png)

Now we need to hit "choose" in the VirtualBox application.

![](/assets/posts/metasploitable-2-on-virtualbox/picture10.png)

And hit the create button to continue with the installation.

![](/assets/posts/metasploitable-2-on-virtualbox/picture11.png)

And we are done. Congratulations as we have now installed our first virtual machine. To power on the machine, we can click on the run button at the top or double click on the Metasploitable icon on the left.

![](/assets/posts/metasploitable-2-on-virtualbox/picture12.png)

Thank you for reading. :+1: