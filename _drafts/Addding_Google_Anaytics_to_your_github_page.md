---
layout: post
title:  "Adding Google Analytics to GitHub Pages"
author: serdar
categories: [ tutorial ]
image: assets/images/17.jpg
tags: [featured]
---

Quick post today on how to add Google Analytics tracking to your GitHub pages site. First, head over to Google Analytics and sign up. After entering your details and green lighting the T&C’s you’ll be directed to an admin page. This will give you the tracking code that you need to add to each page of your site. Mine, anonymised, is below:

<script>
    (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
    (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
    m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
    })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
    ga('create', 'UA-########-#', 'auto');
    ga('send', 'pageview');
</script>


Jekyll makes adding this easy; create a HTML file in your _includes folder containing this code. I named mine google_analytics.html. Then add the following to your default layout, _layouts/default.html:

{% include google_analytics.html %}
Within a few hours Google Analytics should pick up the change, and you’ll be capturing session times, demographics, and other useful information on visitors to your site.

Thanks to Joshua Lande for his original post.