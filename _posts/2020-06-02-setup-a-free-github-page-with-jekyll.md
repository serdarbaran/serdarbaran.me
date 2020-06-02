---
layout: post
title:  "Setup a free GitHub page with Jekyll"
author: serdar
categories: [ Jekyll, tutorial ]
image: assets/images/jekyll/1.png
---

This is a quick tutorial for if you would like to create GitHub page and find out some tricks how to perfect it. I will be going through the steps of how I created my GitHub page.

There will be a time you would want to explore how to create a page for your project, blog ext. 
GitHub provides an easy setup solution for one would to like get the website sorted and host for free. On top that, the smooth integration with own repository system, it enable developers easily modify and update changes on the website. 

There are endless possible way to setup GitHub page and I would like to show you one of them. I have chosen Jekyll as a static site generator. Jekyll is simple to use with your favourite mark-up language and it uses layouts to create a static website. However it is totally up to you which ever site generator you would like use. Also the another reason I preferred Jekyll is simply because GitHub page office webpage looks like get into kind of partnership. 

https://pages.github.com/

![githubpages]({{ site.baseurl }}/assets/images/jekyll/1.png)

**Let's get started**

### Step 1 : Install Ruby

+ Open your command prompt ( terminal for those mac users )

+ First thing you need to install a full Ruby. Jekyll is a Ruby program so you need to install Ruby on your machine to begin with. Head over to the install guide and follow the instructions for your operating system.

    You can install Ruby from the following link - [rubyinstaller.org](https://rubyinstaller.org/downloads/)

    If you would like to check the version number or whether it is properly installed, then type 

    ```
    ruby - v
    ```

### Step 2 : Install Jekyll and bundler gems. 
+  You can carry on using command prompt but I would like to switch to Visual Studio Code and "File>Open Folder"
    ![vscode]({{ site.baseurl }}/assets/images/jekyll/2.png)

+   Then choose the directory where you want your Github page want be stored. 
    After that, open the terminal in VSCode. As you can see in this example my directory is `"C:\Users\serda>"`
    ![vscode_terminal]({{ site.baseurl }}/assets/images/jekyll/3.png)

+   Now install Jekyll with the following command;
	```
    gem install jekyll bundler
    ```
    ![vscode_terminal_jekyll_bundler]({{ site.baseurl }}/assets/images/jekyll/4.png)

### Step 3 : Create a new Jekyll site
+   Create a new Jekyll site at ./myblog
    ```
    jekyll new yourblogname
    ```
	<div class="note" style="color:orange">Note: Now I need to mention something about the repository page name criteria. It cannot be different the owner user name. Otherwise it doesn't work. The criteria is GitHubUsername.github.io</div><br>
    
    ![jekyll_new_blogname]({{ site.baseurl }}/assets/images/jekyll/5.png)<br>
    In this instance the page's name is serdarbaran.github.io. As you can see above, the page is created. 

+   Change into your new directory.
    ```
    cd myblog
    ```
    For example;
    ```
    PS C:\Users\serda> cd .\serdarbaran.github.io\
    PS C:\Users\serda\serdarbaran.github.io> 
    ```
+   You need Bundler to resolve these dependency conflicts. Use Bundler to install all the needed Ruby gems
    ```
	bundle update
    ```
+   Build the site and make it available on a local server.
	```
    bundle exec jekyll serve
    ```
    ![bundle_exec_jekyll_serve]({{ site.baseurl }}/assets/images/jekyll/6.png)

    In fact there are two commands,
	- `jekyll build` - Builds the site and outputs a static site to a directory called _site.
    - `jekyll serve` - Does the same thing except it rebuilds any time you make a change and runs a local web server at.

+   Browse to http://localhost:4000 ( In this example it is http://127.0.0.1:4000/ )
    Your website should look like below
    ![website_overview]({{ site.baseurl }}/assets/images/jekyll/7.png)

### Step 4 : Go live on GitHub
+   Jump back to GitHub and create a new repository
    As I mentioned before the repository name cannot be different the owner user name. Otherwise it doesn't work.
	
    I will give a name, `serdarbaran@github.io` and create the repository.
    ![new_github_repository-1]({{ site.baseurl }}/assets/images/jekyll/8.png)
    ![new_github_repository-2]({{ site.baseurl }}/assets/images/jekyll/9.png)
    <div class="note" style="color:orange">Note: If you custom domain, you can place it in the settings section you can see above.</div>

+   Now go to your repository. You can either use GitHub desktop application or simply upload all the files in the directory directly into the new repository. 
    ![new_github_upload]({{ site.baseurl }}/assets/images/jekyll/10.png)

    I am hoping you did not have any problem so far. Now your Github page should be live. 

    ***…and you're done!***

+   Fire up a browser and go to [https://serdarbaran.github.io.](https://serdarbaran.github.io)

***Congratulation! Your page is live!***

If desired to use different template, you can find many free templates online. Don't forget to check github. 

Thank you for following my tutorial. I hope you found it useful for you.

If you like it, please don't forget to share it.