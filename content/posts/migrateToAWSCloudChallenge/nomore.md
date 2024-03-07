---
draft: true
title: How this site is deployed for free with Hugo, GitHub and Netlify
subtitle: And how you can do it too!
date: 2021-01-15
description: >-
  Article showcasing how this site is deployed with free tools
tags:
  - hugo
  - setup
aliases:
  - how-to-deploy-with-netlify
---

In this post I will showcase how this site is quickly deployed using free tools.
<!--more-->

Deploying a site like this is very easy and straightforward. This is not so much a tutorial, but its an outline of what I did to get it running.  
You can try following along, but bear in mind that its not a full step by step guide.  

## Choosing the platform: Hugo

I wanted a quick and easy way of posting stuff on the internet, so I could've used stuff like Medium, Blogger, WordPress, or other similar services. But I also wanted to own my data, so they are out. Hosting something myself is the solution to this.  
I also wanted something really easy to manage with little overhead, so WordPress, Drupal and similar, while being very powerfull, are also out.
Enter Static Site Generators (SSG), fantastic tools that generate statis HTML files from plain text (usally markdown) and a few config files! There are many options, all with different qualities and objectives. Hugo, Jekyll, Ghost, etc.  
All of them have pros and cons, and which one you use would depend on your needs and how familiar you are with the lenguage they are programmed in.  

In my case, I choose Hugo (I used Jekkyl for a while in the past), because its a single, very fast binary. And out of the box it includes all the features I wanted. 

## Installing and setting up a git repo

I pretty much followed the [getting started tutorial](link) from Hugo, and created a public GitHub repository for it.  
I do most of the writting and testing for the site, on my Manjaro laptop, and the Hugo server is running most of the time so that I can go an look at changes. Its amazing how fast it compiles everytime it senses any change to content or files.
Choosing a theme was difficult, I wanted something that was not too flashy, and more focused on the text itself. I found some cool looking ones, but they had a lot of extra features that I didn't want. But I finally stumbled upon [smeagle](link), which I think its fantastic! I really recommend it.
