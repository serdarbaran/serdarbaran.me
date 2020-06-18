---
layout: post
title:  "Top Things to Do After Installing Kali Linux"
author: serdar
categories: [ Kali, Tutorial, Linux ]
image: assets/images/top_things_to_do_Kali/10.jpg
tags: featured
---
Kali Linux distribution is highly customizable. It, by default, doesn’t have everything you need to get you through day-to-day use with ease. The various things that can be done to improve your interaction with the operating system depends on how comfortable you feel in using it. With a few changes in the settings and applications, you can quickly get started in using Kali like a professional white hat.

### 1. Create a New Low Privileged User
Creating a new low privileged user goes top on my list. Let’s get one of the most important things right in the first place. It is strongly advised to open many applications like the Chromium Browser and the Tor Browser with low privileged user. Such applications rely heavily upon low-level permissions to deliver some degree of security.

For many years, Kali was being distributed by default with root user. Recently, Kali moved to a “traditional default non-root user” model. However if you are using root user, moving to non-root user is suggested to mitigate a security risk which make the host to be compromised more difficult.

You can add a new user by using the following command;
```
$ sudo adduser newuser
```
It will ask user password and some extra information before completing the process. 
Note: By default, sudo requires that users authenticate themselves with a password. This is the user’s password, not the root password itself.  
![add_new_user]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/11.png)

You should double check if the new user is added successfully by
```
$ awk -F: '{ print $1}' /etc/passwd
```
![check_add_new_user]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/12.png)

### 2. Update, Upgrade, & Dist-Upgrade
I assume you downloaded the latest version of Kali. But again it is worth to check you have the latest of everything and update your workstation’s dependencies.
```
$ sudo apt-get clean 
$ sudo apt-get update 
$ sudo apt-get upgrade -y 
$ sudo apt-get dist-upgrade -y
```
![apt-get_clean]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/13.png)
![apt-get_upgrade]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/14.png)

### 3. Install Git
Git is a free and open source distributed version control system and commonly used in Linux. 
Git can be installed by using the command below;
```
$ sudo apt-get install git
```
![install_git_on_kali]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/15.png)

### 4. Customization of Kali Linux’s Look
If you would like to tweak on how your Linux’s look, I would like to recommend gnome-tweaks tool. This is a desktop customization and setting manager for Gnome desktops.
```
$ sudo apt-get install gnome-tweaks-tool
```
![install_gnome-tweaks]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/21.png)

### 5. Install Tor Browser
The Tor (The Onion Router) provides anonymity and privacy to users. With Tor, you could potentially prevent third party tracing your activity back to your IP address. The traffic that passes along the Tor network is encrypted. 

Open a terminal window
```
$ sudo apt-get update

$ sudo apt-get install tor torbrowser-launcher 
```
and select Y at the prompt
![install_tor]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/18.png)

For the first time, it will download some packages
![install_tor_2]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/19.png)

&#9888; Note: If you’re running Kali Linux as root, you might get an error saying you can’t run Tor as root. You should switch to less privileged user. 

### 6. Install Anti-Virus Program
If you have a preferred Antivirus Program with a licence, go for it. If you don’t want to pay and are looking for a free program, you might consider checking ClamAV, ClamTk, ChkrootKit, RookKit Hunter,Sophos and F-PROT. 

For example ClamAV can be installed by:
```
$ sudo apt-get install clamav
```
![install_clamav]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/17.png)

### 7. Install your favourite code editor
Two very popular code editor comes to my mind for Linux. One of them is Atom and the other one is VS Code. Pick one of them to install. I will go with Atom.

+ First change the directory into your Downloads folder, or wherever you have downloaded the file to.
```
$ cd /home/kali/Downloads/
```
+ Secondly to install Atom Linux distribution, add Atom's official package repository to your system by running the following commands:
```
$ wget -qO - https://packagecloud.io/AtomEditor/atom/gpgkey | sudo apt-key add -
$ sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
$ sudo apt-get update
```
+ After that install Atom
```
# Install Atom
$ sudo apt-get install atom
# Install Atom Beta
$ sudo apt-get install atom-beta
```
+ Alternatively you can install .deb package and install it directly
```
# Install Atom
$ sudo dpkg -i atom-amd64.deb
# Install Atom's dependencies if they are missing
$ sudo apt-get -f install
```

![install_atom]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/16.png)	

### 8. Install Terminal Multiplexer
Multiplexer terminal emulator divides the window into several sub-windows to help you do many things in one window. There are many multiplexers available for free. Probably by now you’re asking : “But which one should I use?” - the answer to that is “The one that suits you best”. More or less they are all the same. It is a program that manages the terminal window and is a good tool to use in terms of information gathering.

For example you can install one of them called Tilix by the following command:
```
$ sudo apt-get install tilix
```
Once the installation is completed, type `tilix` in the command window to run tilix

![install_tilix]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/20.png)

---
Those are the Top Things I prefer to do after installing Kali Linux. These installed packages and settings makes my work on Kali much faster and easier. I would like to remind again that it is important you know you can be at risk when running your OS as root. It is definitely recommended to use low privileged user account for beginners. Keep my recommendations in mind and you will have created yourself an extra layer of protection.

As I mentioned at the beginning of the article, this list is ongoing, so make sure to check back! Feel free to let me know your first to do when you install Kali!

<!--[Don't forget to check my github page!](https://serdarbaran.github.io/) &#9822;-->