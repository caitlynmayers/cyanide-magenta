---
layout: post
title:  "A New Website"
date:   2016-02-21 09:00:00
categories: design development
---
It's finally alive! I've been working on my new site off and on for a few months now, making slow progress on the nights, mornings and weekends around work, and I am thrilled that the new site is finally ready to deploy.

My old website needed a complete overhaul *badly*. When I first created a website back in college, I started with a Flash site *shudders*. I quickly became a Posterous convert because of my classmate [Jason Lang](http://www.jasonlang.me), and my sites lived on that service until they were acquired by Twitter in 2012 and shut down their service the following year. Posterous created a very nice Wordpress export plugin, and since most of the sites I worked with professionally were Wordpress sites, I decided to go with that as my new site's platform. I wasn't as comfortable with code then as I am now, so I chose to buy a theme someone else designed and built and did some code modifications to get it where I wanted it to be.

### The old

When I created that new site, Wordpress 3.6 was the most recent release. I went in to update the WP to 3.7 and it absolutely broke everything with the theme, so I needed to fix the theme in order to use a stable release. I didn't want to begin digging through someone else's work like that, so I left it alone knowing I'd need to fix it. Once the site was old enough, I started to see hacking becoming an issue, and I couldn't upgrade plugins because I couldn't upgrade the WP build. The WP configuration with the theme wasn't great and the site was *way* too bloated. I decided that I needed to start over with something new and began looking into static site generators.

### Jekyll, Middleman or Pelican?

My new site did not need any of the benefits of a database, and I knew that speed and performance would be dramatically improved by using a static site for this site. I researched the top 10 static site generators, eventually narrowing the field down. I had three top contenders - Jekyll, Middleman and Pelican. While I would've loved to learn Python on this project, I didn't think it was the right project for me to cut my teeth on it, so I've saved Python for another day. 

Between Middleman and Jekyll, I liked that Middleman seemed to have more features right out of the box, things like image minification, uglification, etc. What I didn't much care for is that it seemed to have way more features than I needed and I did not want to spend time dealing with the cruft - one of the main reasons I wanted to get away from Wordpress.

I decided to go with Jekyll after all of this research for a few important reasons: it has the best support and most active dev community, which meant that working in an entirely new platform would be much easier because of those resources; it uses Liquid as its templating language, which meant I would be learning the templating language of Shopify and could use that in the future; and it was easy to spin up and deploy on almost any platform I chose.

##### Some tech specs

So I built my new site with Jekyll, and I really enjoyed it. I used HTML/CSS only for the site - didn't really feel like it was necessary to use any Javascript since there isn't anything that requires heavy lifting. I used Flexbox for the first time to do some stuff that had previously been done with Javascript, and I'm really excited about the future with Flexbox. I used [Simple Form](https://getsimpleform.com) for my contact page, and it was a breeze to implement. There are a lot of assets that have been minified, and I'd like to reduce their size even further. I know my CSS could use some refactoring for performance and I'd love to refactor it in [BEM](http://getbem.com) style, but I'll save that for another day.

##### Some other new stuff
Aside from the new site, there's all new [About Me](/about) content that explains what the whole Cyanide & Magenta thing means and there are 6 brand new [case studies](/case-studies) featuring some of my favorite work.

I'm very excited that I've completed this project and am looking forward to my next Jekyll project!