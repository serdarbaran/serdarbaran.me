---
layout: post
title:  "Top Things to Do After Installing Kali Linux"
author: serdar
categories: [ Kali, tutorial ]
image: assets/images/top_things_to_do_Kali/10.jpg
tags: featured
---
Kali Linux distribution is highly customizable. It, by default, probably doesn't have everything you need to get you through day-to-day use with ease. 
There are just many things can be done to improve your interaction with the operating system depends on how you feel comfortable to use it.

With a few changes in the settings, and applications, you can quickly get started using Kali like a professional white hat.

### 1. Create a New Low Privileged User
Creating a new low privileged user goes top in my list. Let's get one of the most important thing right in the first place.
It is strongly advised to open many applications like the Chromium Browser and the Tor Browser with low privileged user. Such applications rely heavily upon low-level permissions to deliver some degree of security.

For many years, Kali was being distributed by default with root user. Recently, Kali moved to a “traditional default non-root user” model. However if you are using root user, moving to non-root user is suggested to mitigate a security risk which make the host to be compromised more difficult.

You can add a new user by using the following command;
```
$ sudo adduser newuser
```
It will ask user password and some extra information before completing the process. 
Note: By default, sudo requires that users authenticate themselves with a password. This is the user's password, not the root password itself. 
![add_new_user]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/11.png)

You should double check if the new user is added successfully by 
```
$ awk -F: '{ print $1}' /etc/passwd
```
![check_add_new_user]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/12.png)

### 2. Update, Upgrade, & Dist-Upgrade
I assume you downloaded the latest version of Kali. But again it is worth to check you have the latest of everything and update the your workstation's dependencies.
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
If you would like to tweak on how your Linux's Look, I would like to recommend gnome-tweaks tool. This is a desktop customization and setting manager for Gnome desktops.
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
If you a preferred Antivirus Program with a licence, go for it. If you don't want to pay and looking for a free program, you might consider checking ClamAV, ClamTk, ChkrootKit and RookKit Hunter,Sophos and F-PROT. 

For example ClamAV can be installed:
```
$ sudo apt-get install clamav
```
![install_clamav]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/17.png)

### 7. Install your favourite code editor
Two very popular code editor comes to my mind for Linux. One of them is Atom and other one is VS Code. Pick one of them install. I will go with Atom.

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
Multiplexer terminal emulator divides the window several sub-windows to help you to do many things in one window. There are many multiplexer available free. Probably by now you're asking : "OK, I get it, but which one should I use?" - the answer to that is "The one that suits you best". More of less they all same. It is a program that manages the terminal window is good tool to use in terms of information gathering. 

For example you can install one of them is call Tilix by the following command:
```
$ sudo apt-get install tilix
```
Once the installion is completed, type `tilix` in the command window to run tilix

![install_tilix]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/20.png)

---
If I haven’t forgotten anything, those are the Top Things I prefer to do after installing Kali Linux. These installed packages and settings makes my work in on Kali much faster and painless. I would like to remind again it is important that you understand that you can be at risk when running your OS as root. It is definitely recomended to use low privilaged for beginners. Keep my recommendations in mind and you have created yourself an extra layer of protection.

As I mentioned at the beginning of the article, this list is ongoing, so make sure to check back! Feel free to let me know your first to do when you install Kali!

<!--[Don't forget to check my github page!](https://serdarbaran.github.io/) &#9822;-->