---
layout: post
title:  "Free Customisable Financial Stock Screener"
author: serdar
categories: [ Screener, Finance, YahooFinance ]
image: assets/images/top_things_to_do_Kali/10.jpg
tags: featured
---
There are lot of stock screener out. Many websites have been trying to atract users to create an account by offering free screeners. Cross-selling seems be modern way of business approach nowadays. For those screener have complexity to and flexibility to modified, most likely won't come free. However would you like to create quickly your one and create an interactive graphs will help you to make a decision? 

In this article, I provided step-by-step how to code a screener by using python and jupiter notebook. For data source, I decided to use Yahoo finance as I believe it is still one of the best free financial information provider. Lastly I choose plotly to create interactive graphs. 

Lets see it went? 

### 1. First Step - Decide how to source the data
I get it, the are many ways to scrap data online. You can easily find an article to teach you how to get each single data from the website. Only problem is the process is long and if you are new in this, you may find it difficult not to get blacklisted if you scrap large amount of data. Therefore it is not recommendend to go down in that road. However wouldn't want to use an easier way to get financial information from Yahoo Finance? There are few packages can be found which will make the life easier. Such as [yahoo-finance](https://github.com/lukaszbanasiak/yahoo-finance) , [yfinance](https://github.com/ranaroussi/yfinance) , and [yahooquery](https://github.com/dpguthrie/yahooquery). Among all these, in my view yahooquery is the one will bring us the success easiest with simple useage. 

First install it 
```
pip install yahooquery
```

Then it is time to creating our code
```
from yahooquery import Ticker
from yahooquery import get_exchanges
from yahooquery import Screener
```

### 2. Creating dataframes
With yahooquery, you can analyse individual financial derivatives, but also using their cool ready screener to get informations of large amount of stocks and commodities is possible. 

```
s = Screener()
s.SCREENERS # View available screeners along with description and nice name
# or just view list of keys
s.available_screeners
```
You will see so many already defined screener. From the list, pick which industries you are interested in or simply choose other already defined categories

For the demonstration, I will randomly choose biotechnology,security_software_services,wireless_communications,technical_system_software,gaming_activities and growth_technology_stocks.

```
list_screeners = ['biotechnology','security_software_services','wireless_communications','technical_system_software','gaming_activities','growth_technology_stocks']
```




```
$ sudo adduser newuser
```
It will ask user password and some extra information before completing the process. 
Note: By default, sudo requires that users authenticate themselves with a password. This is the user’s password, not the root password itself.  
![add_new_user]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/11.jpg)

You should double check if the new user is added successfully by
```
$ awk -F: '{ print $1}' /etc/passwd
```
![check_add_new_user]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/12.jpg)

### 2. Update, Upgrade, & Dist-Upgrade
I assume you downloaded the latest version of Kali. But again it is worth to check you have the latest of everything and update your workstation’s dependencies.
```
$ sudo apt-get clean 
$ sudo apt-get update 
$ sudo apt-get upgrade -y 
$ sudo apt-get dist-upgrade -y
```
![apt-get_clean]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/13.jpg)
![apt-get_upgrade]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/14.jpg)

### 3. Install Git
Git is a free and open source distributed version control system and commonly used in Linux. 
Git can be installed by using the command below;
```
$ sudo apt-get install git
```
![install_git_on_kali]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/15.jpg)

### 4. Customization of Kali Linux’s Look
If you would like to tweak on how your Linux’s look, I would like to recommend gnome-tweaks tool. This is a desktop customization and setting manager for Gnome desktops.
```
$ sudo apt-get install gnome-tweaks-tool
```
![install_gnome-tweaks]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/21.jpg)

### 5. Install Tor Browser
The Tor (The Onion Router) provides anonymity and privacy to users. With Tor, you could potentially prevent third party tracing your activity back to your IP address. The traffic that passes along the Tor network is encrypted. 

Open a terminal window
```
$ sudo apt-get update

$ sudo apt-get install tor torbrowser-launcher 
```
and select Y at the prompt
![install_tor]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/18.jpg)

For the first time, it will download some packages
![install_tor_2]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/19.jpg)

&#9888; Note: If you’re running Kali Linux as root, you might get an error saying you can’t run Tor as root. You should switch to less privileged user. 

### 6. Install Anti-Virus Program
If you have a preferred Antivirus Program with a licence, go for it. If you don’t want to pay and are looking for a free program, you might consider checking ClamAV, ClamTk, ChkrootKit, RookKit Hunter,Sophos and F-PROT. 

For example ClamAV can be installed by:
```
$ sudo apt-get install clamav
```
![install_clamav]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/17.jpg)

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

![install_atom]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/16.jpg)	

### 8. Install Terminal Multiplexer
Multiplexer terminal emulator divides the window into several sub-windows to help you do many things in one window. There are many multiplexers available for free. Probably by now you’re asking : “But which one should I use?” - the answer to that is “The one that suits you best”. More or less they are all the same. It is a program that manages the terminal window and is a good tool to use in terms of information gathering.

For example you can install one of them called Tilix by the following command:
```
$ sudo apt-get install tilix
```
Once the installation is completed, type `tilix` in the command window to run tilix

![install_tilix]({{ site.baseurl }}/assets/images/top_things_to_do_Kali/20.jpg)

---
Those are the Top Things I prefer to do after installing Kali Linux. These installed packages and settings makes my work on Kali much faster and easier. I would like to remind again that it is important you know you can be at risk when running your OS as root. It is definitely recommended to use low privileged user account for beginners. Keep my recommendations in mind and you will have created yourself an extra layer of protection.

As I mentioned at the beginning of the article, this list is ongoing, so make sure to check back! Feel free to let me know your first to do when you install Kali!

<!--[Don't forget to check my github page!](https://serdarbaran.github.io/) &#9822;-->