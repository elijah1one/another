---
layout: post
title: "URL Fields in Jekyll Config.yml"
date: 2016-09-20 11:00:00
image: '/assets/img/'
description: 'A post about using your custom URL in a Jekyll theme. How to set the baseurl and url field in config.yml. '
tags:
- Github
- Jekyll Themes 
categories:
- Jekyll 
twitter_text: 'How to Set Base URL and Domain in Jekyll Themes'
---

I just set up a Jekyll site for a friend, and ran into the dreaded old problem of CSS not rendering when the custom domain was done propogating. I forgot that some explanations on the web are rather confusing when it comes to this point. Basically, if you are downloading a theme (like mine here) from [Jekyllthemes.org](http://jekyllthemes.org), you will have to "configure" the config.yml (aptly named) to get your site working with a custom domain. These instructions are important for hosting on Github pages. 

The easiest way to understand this is that the baseurl is not needed if you are placing a custom domain in the url field. If you put the baseurl in while using a custom domain, you will not have any CSS! This is because the style file will look for the site [http://weboholic.xyz/theme](http://weboholic.xyz) instead of just the bare domain. I really hope that makes sense! 

So forget the other guides you've seen online. Just remember to get rid of the baseurl and throw your domain in the url field, while also making sure that your domain has been added correctly in settings. There is also the issue of setting your A Records with your domain company. 

CSS may also fail in Jekyll for another reason. Sometimes the path in the head of the site will have a "/" in front of it which could cause some conflicts when rendering. We will look at this in another session. 
