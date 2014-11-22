---
layout: post
title:  "Came to tweet about a Docker error in CircleCI; left with the best Twitter UI bug ever!"
date:   2014-11-22 10:15:00
categories: development user-interface bugs twitter docker circleci
permalink: /2014/11/22/i-found-the-best-twitter-ui-bug-ever
comments: true
---

I almost didn't share this because I actually enjoyed accidentally finding and experiencing this bug. And I had way too much fun showing it to anyone that happened to stroll past my desk in the last two days!

<iframe width="740" height="450" src="//www.youtube.com/embed/xRLigdfAh8E" frameborder="0" allowfullscreen></iframe>

I didn't dig into the page source to see if this looked intentional therefore I choose to believe it is a kick ass UI bug! (Although I kind of want it to stick around now.)

### Reproduce Me, If You Can

I found this bug following a "Follow" link in an automated email notifcation from Twitter.

1. Locate an email from Twitter with a subject like: "xxx just replied to one of your Tweets!" I *think* the email needs to originate from a Twitter user that you are not already following in order to land you on the correct page.

2. Click the "Follow" button provided in the email.

3. After the page loads, mouse in and out of the "Follow" repeatedly, as seen in my screen recording.

4. Laugh hysterically as you watch their profile picture slowly ascend into oblivion!

[![twitter-email-screenshot]][twitter-email-screenshot]

### Oh no! I can't have fun once the profile pic has went the way of the birds!
You will be pleased to see that a simple refresh will bring back the fun.

At first I assumed the link was one time use, so I didn't refresh it until I had tried to manually reset the positioning with CSS in development tools. This is also the reason why I hid the URL bar in my screen recording. I noticed, after sharing the link with a friend, that it created enough of a session to follow/unfollow that user, but I am not sure if that link fully creates a valid session for the user. If so, I didn't want to hand out access to my Twitter account.

### Protip
For ultimate enjoyment, ask others to come over and look at your screen. But, when you ask them, do it in a very serious, monotone voice as if you have found a heart bleeding poodle wearing a shell going into shock. Then proceed to demonstrate. =D

Awesome tip: Subscribe, share my video...all of that stuff. I mean, I worked really, really hard for like 10 minutes to record, upload, and write this much too long description.

### Coincidences Make Life Interesting and lulzy!
Ooooooh, yeah, what made this even more awesomerest™ is that I found this because I was tweeting at CircleCI about a Docker error that kept breaking my CI runs. I don't use Twitter often, and I certainly don't follow links in Twitter emails, so it was unlikely that I would have seen this already had it not been for that Docker issue. I guess it partially makes up for all of the head banging and "Still trying to figure out the problem" commits that occured.

### ¯\\\_(ツ)_/¯ MOAR BUG (not Twitter related)
Comically, I went to gfycat.com to create a short gif from my Youtube video and was unable to do so due to a bug. When I put in the url of the youtube video it usually asks for a start time and duration. For some reason, that part of the form is no longer in the dom. (I dug into the dom and looked with developer tools.) Yet, the API is obviously still expecting it.

[![gfycat-ui-bug][gfycat-ui-bug]][gfycat-ui-bug]

[twitter-email-screenshot]: /images/posts/2014/11/twitter-ui-awesome-bug-email-screenshot.png
[twitter-bug-cover]: /images/posts/2014/11/best-twitter-bug-thumb.png
[gfycat-ui-bug]: /images/posts/2014/11/tried-to-make-a-gfycat-found-moar-bug.png
