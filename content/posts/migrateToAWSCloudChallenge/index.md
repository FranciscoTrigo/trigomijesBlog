---
draft: true
title: "Cloud resume Challenge: Deploying with Amplify and S3"
subtitle: "Also migrating from Netlify"
date: 2021-01-15
description: >-
  Article showcasing how I migrated this site from Netlify to AWS Amplify
tags:
  - hugo
  - AWS
series:
  - Cloud Resume Challenge

---

I am doing the [Cloud Resume Challenge](https://cloudresumechallenge.dev/), but the domain that I wanted to use for it was already being used for this blog, and it was deployed with Netlify. Here is how I migrated it over.
<!--more-->

Netlify is very useful for deploying static sites like this (I'm using Hugo), and I've used it for a while, both for this blog and other sites in the past. However, I decided to migrate to AWS because of the Cloud Resume Challenge and because I want to have more hands-on experience with AWS.  

Here is what I needed to do:

- Migrate my domain out of Google domains (now acquired by Squarespace)
- Set up my domain with Route53
- Use AWS Amplify to deploy this blog from GitHub
- Set up DNS records so I can receive emails in my domain

## Migrating my domain

I used Google Domains for a long time, but they recently sold their domain register business to Squarespace. I do not have anything against Squarespace, but I've been migrating all of my domains to [Porkbun](https://porkbun.com/) before they completely take over.  
This was as easy as unlocking my domain in its settings and then requesting the migration to Porkbun, I had to pay a small fee of around $10 USD, and then accept the migration from Google's side.  
I could've also migrated the domain to AWS, but I don't want to have my domains scattered among many registrars.

## Seting up the domain with Route53