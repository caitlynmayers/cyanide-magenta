---
layout: post
title:  "I'll Never Use Squarespace Again"
date:   2013-12-19 09:11:03
categories: development squarespace
---

[I am not a developer. I am a designer.*](#update) Somehow that doesn’t stop me from getting my hands dirty in the land of the web, and I will, on occasion, take on building a website myself. I have extensive experience with WordPress (my personal site is powered by it) and have worked with Expression Engine and decided that I wanted to give Squarespace a try for this next site. I chose Squarespace for several important reasons: they provide 24/7 support for the client, have a sweet e-commerce platform built-in (the client is a retail store), have one of the most intuitive admin panels (which means clients are less likely to mess things up than in WordPress), and their JSON templating system and supporting documentation made me weak in the knees.

I presented my case to the client and they agreed that Squarespace seemed like a great fit for them, so I proceeded to set up the site for them, purchasing the $24/month Business plan that gave both the client and me access to the full set of features the site would need to function smoothly.

Setting up the site was a dream – I had everything configured to have a test site up and running in 5 minutes. Turning developer mode on couldn’t have been easier, and accessing the site’s Git repo was one of the easiest set-up experiences I have encountered. I am not a developer, but I am well-versed in CSS and HTML, and am now dabbling with .js and JSON. I turned on developer mode so I could access the code and make minor adjustments to the site’s responsive tweak points. I wasn’t going in to completely tear down the base template and reconstruct an unrecognizable rework of the template, I was purely going in to make an occasional font-size: adjustment here, a max-width: adjustment there.

I wrapped up the test site layout and began the QA phase to make sure there weren’t any major issues with the site. Everything worked great except for the navigation for <768px screens – which is a major bug. >768 px screens have a parallax effect enabled, and that nav is a different nav from the <768 nav, which is an off-canvas nav. I set the site up as a 1 page parallax site and used anchor tags in the nav to keep it 1 page and maintain the nav nodes the way I wanted them (because of this Squarespace template’s pagination, setting up the site hierarchy/structure this way was the simplest way achieve the 1 page effect).

I decided to dive into the .js to see what was going on. Truthfully, I had no idea what was going on. I noticed that there were event handlers for the parallax nav but not for the mobile nav, and every hack I tried didn’t fix it (that, of course, wasn’t the issue). I then shrank my browser window and ran the inspector to see if I could see any anomalies that way. I noticed that every time I clicked the link in the nav, the url would change to the appropriate anchor tag, but then immediately reverted to the home url with the landing anchor, which seemed to confirm, to me, that there was something amiss with the template itself. I looked on the forums and saw others had the same issue, and then got in touch with Squarespace support to file a bug report. I gave them the info I had, they confirmed it was a bug and that it was being worked on, and yesterday – about 2 weeks later – they emailed me to let me know that the bug had been fixed. Great!

Then I made the mistake of asking Squarespace for the code. Here’s the email thread:

Caitlyn DEC 18, 2013  |  02:22PM EST

Can you send me the code that fixed it? I’ve got my site in Developer mode and need the fixes so I can push it to my site.

–

Tim A. (Squarespace Customer Care) DEC 18, 2013  |  02:46PM EST

Hiya Caitlyn,

Unfortunately we don’t offer support in that particular way, we’re only able to offer support that deals with trouble-shooting within the confines of our CMS. At this time i can’t provide code to fix this particular issue.

I hope this answered your questions and we’re here 24/7 so drop us a line anytime! :-)

–

Caitlyn DEC 18, 2013  |  02:54PM EST

So how am I supposed to implement the fix on my website?

–

Caitlyn DEC 18, 2013  |  03:08PM EST

Let me rephrase – I cannot fix the site without someone from Squarespace providing me with the code that fixed the bug. If you cannot provide me with that code, can you put me in touch with the person that can or provide me with a solution that gets me the code?

–

Chris L. (Squarespace Customer Care) DEC 18, 2013  |  03:18PM EST

Hi Caitlin,

When signing up for a Developers account or toggling the Developer Tools on a template, we cannot fix bugs related to the template because developer templates will no longer receive fixes for template specific bugs. The developer/account owner would then be responsible for those fixes. This is why we are not able to provide the code that fixed the issue.

You could certainly turn off the Developer Tools and go back to a regular, supported template, however you would loose any custom work that has been done on the developer side.

Since we don’t provide support for troubleshooting or creating custom code, you may be interested in joining Squarespace Answers — This is a community where customers and developers discuss the Squarespace platform in a Q&A format:

http://answers.squarespace.com

As a note, Answers accounts are independent from your Squarespace account. If you haven’t done so, you can sign up for Answers here.

Let us know if you have any additional questions. Thank you.

***

This pissed me off. I understand that Squarespace can’t just push template updates to the repo, but I don’t understand why they won’t in any way notify theme users with developer mode enabled that there have been bug fixes, talk about what code was edited to implement the fixes and then say here are the updated template files – merge them at your own risk. I cannot fathom this supposedly developer-friendly platform sandboxing developers like this, and the more I thought about it, the more irritated I became.

This pissed me off so much that I went on their website and engaged a live chat support person to hash this out with.

Ron A.: Hi there, how are you doing!

Me: I’m very pissed off at you. I’m trying to get a bug fix resolved and your support team doesn’t seem to understand that the fix is simple to accommodate – let me look up my ticket # 744637

Ron A.: I’m sorry, please understand that our support team does not resolve bug issues, we send them to our developers and they prioritize them. I can take a look at the case and speak with someone about it.

Me: there was an issue with the mobile navigation in the marquee theme, so I submitted the ticket to have the theme developers look into the code to fix their issue – which they were able to do.

Ron A.: I see that you have turned on the dev toggle

Me: and I was notified of it. I do have developer mode turned on

Me: I needed to make minor adjustments to the CSS to tweak the theme. I haven’t touched anything else – it’s as was provided in the git repo to me from you. All I need is a copy of the code that fixed the bug that came with the theme and is still occurring through no fault of my own in the theme files you provided me. It seems that there’s no way for me to obtain that without it being a royal pain in the ass. All you need to do is send me the files that were changed to fix the bug.

Ron A.: If you turn on the dev toggle you will not receive updates, this includes bug fixes.

Me: That’s bullshit and you know it – all I need are the code fixes.

Ron A.: We are unable to provide code support or solutions.

Me: Well what the f*ck did I sign up for then? I can get the updated code if I create a new account and pay for developer access and then access the git repo and download the files and merge the bug fixes into my own code, which will cost me another $21 bucks. And that’s a total bullshit solution.

Ron A.: I ask that you please refrain from using vulgar language.

Me: When all you have to do is tell me what to fix and how to fix it and your problems will go away. I’m sorry, but I’ve been dealing with completely unhelpful support personnel all day and this is totally unacceptable.

Ron A.: Developer templates will no longer receive fixes for template bugs. The developer/account owner would then be responsible for those fixes. We are not able to provide you with the fix or the code for the fix.

Me: It’s not that hard for you guys to provide me with the information that I need to fix the issue that is in your template that you didn’t construct properly. So. let’s come to a conclusion here. The only way for me to actually get the template files with the fix implemented is for me to completely wipe out the git repo I have and start over with a new one that includes the recently pushed fix from your developer.

Ron A.: That is correct.

Me: that’s bullshit. I’m sorry but that’s totally nuts. I should be able to download the files without wiping out my repo and integrate them at my own risk. It’s just insane for you to not provide me with any access to a critical bug fix.

Ron A.: I understand and I am very sorry, however we are unable to accommodate this request. Turning on the Dev Toggle assumes all responsibility for all bug fixes as it assumes that the developer would know how to fix these issues. It is our policy not to provide support for code based solutions and we do not push fixes out to Developer accounts since that fix can break a piece of code that the developer has added.

Me: I understand why that’s your policy (CYA) but I am highly disappointed. My Squarespace experience had been incredibly pleasant until this point, and this impasse is incredibly frustrating. It boggles my mind that you are unwilling to provide any method through which I could easily obtain the bug fixes without losing my current code or having to pay for an additional developer account, and this will be the first and last time I use Squarespace for my web needs.

Ron A.: Again I am very sorry for this. Please do understand that it is not that we are unwilling, but that we cannot provide our code for sites under the developer platform for the reasons I mentioned above. If you have anymore questions I will be happy to help. If not then I will end our session as I can not provide the support you’re requesting.

Me: I understand what you are saying. Thank you for your time.

***

My only Squarespace-provided options were to wipe my repo out and get the fix or to create another site, pay for the additional dev license and get the files that way. Bullshit.

Fortunately, one of the people on the forum had the nav issue on his site and that he didn’t have developer mode toggled. I went to his site, inspected the source, copied the site.js file, pasted it into my repo, pushed the changes and BOOM. Fixed. No issues detected so far. If you have the same issue with your site and you have developer mode enabled on the Squarespace Marquee theme, here’s my .js file so you can drop it in (I still haven’t looked at the code to see what they adjusted to make the nav work).

I was Squarespace’s biggest fan until yesterday, and their unwillingness to provide a simple method to obtain a fix to their code has made me angrier than I’ve been recently. I will never use Squarespace again, and I am saddened by that. I had high hopes for Squarespace becoming my CMS of choice, and I think their handling of this situation is an incredible disappointment to me and the development community.

***

*<a id="update"></a>
I’ve taken the leap and am now a hybrid Designer and Front-end Developer for [CO+LAB](www.teamcolab.com). I’ve quite enjoyed this transition and consider myself a developer now, mostly.

For more on this issue, read my follow-up article:

[I may use Squarespace again after all.](#)