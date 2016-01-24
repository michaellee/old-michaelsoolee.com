---
layout: post
title: "Finally got SSL on my domain and it was free!"
category: work
---

If you're reading this post, you should notice in your browser's URL bar, that I'm serving up this site via SSL. Which as a result you should see `https://` prefixed to my domain and a nice little padlock icon next to the URL.

I've been meaning to get SSL setup for my site, but was dreading the painful process and the price from the last time I did it. Then yesterday, I saw an announcement that [Amazon's AWS provided free SSLs for custom domains](https://aws.amazon.com/blogs/aws/new-aws-certificate-manager-deploy-ssltls-based-apps-on-aws/). After reading the post, I was ready to take the new feature for a spin. Only issue was, I wasn't hosting on AWS but am [currently hosting on DigitalOcean](https://m.do.co/c/af0ae1cd97ec). 

Since my entire site is versioned in git, moving services wouldn't be a big problem. But I was worried about potential downtime from changing DNS records. Usually this wouldn't be a problem, but a few days ago [I had announced my new book]({{site.url}}/writing-first-book) and didn't want to serve up a potential server error if someone was visiting my site as a result of my book announcement. So I decided against AWS' new SSL service.

Combing through the comments of the AWS SSL feature post, I noticed someone mention [Let's Encrypt](https://letsencrypt.org). I had heard of Let's Encrypt before but at the time was hosting my site on GitHub Pages. Now that I'm on a VPS, Let's Encrypt was definitely a viable option. Not to mention, DigitalOcean already had a [guide to setup a Let's Encrypt SSL on an nginx server](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-14-04).

Following the guide, I had SSL setup in just a few minutes. Now my site is served over SSL, I didn't have to pay a dime for the certificate, my site only experienced seconds of downtime from having to restart nginx and it was done all from the command line. If you're looking to serve your site up over SSL and have been hesitating because of the price and setup process, I can't recommend enough giving Let's Encrypt a shot.
