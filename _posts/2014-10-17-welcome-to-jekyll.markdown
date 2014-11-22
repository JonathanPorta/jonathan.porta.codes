---
layout: post
title:  "Welcome to Jekyll!"
date:   2014-10-17 21:44:25
categories: jekyll update
permalink: /2014/10/17/welcome-to-jekyll
comments: true
---
### Hello? Is this thing on? Good.
I have been wanting to switch my blog off of WordPress and over to Jekyll for a very long time. Well, I finally did it.

### Why I Ditched self-hosted WordPress
I was running a self-hosted installation of WordPress. It was slow, hard to change and just felt way too heavy for what I needed. I write posts rather infrequently. In fact, I suck at writing new posts and will use any excuse in the world to not write one and a self-hosted WordPress installation gave me lots of excuses not to write.

For one, it seemed like anytime I would login to write up a post I would be told that I needed to update my WordPress installation. Updating would involve me logging into cPanel, finding phpMyAdmin and making a backup. Then, I would need to fight with WordPress to update, and finally, I could start writing. Of course, maybe I don't need to install every update, but since I don't really follow the stuff that happens in the WordPress community, I have no idea whether I am leaving myself open to hundreds of zero-day exploits or just missing out on a sexier admin interface.

Everytime I would go through this process I would think to myself "Damn, I just want to open up my editor and write out my post." Well, that's what Jekyll lets me do.

### Jekyll: Open your Editor, and Write
This was the main draw for me. Eliminate all of the things that block me from writing, and just make it easy. I really hate WYSIWYG editors, so I would write my posts in plain-text. Then, I would go back to the post and sprinkle in whatever HTML WordPress needed to get the post looking how I wanted. Writing HTML kind of sucks. Jekyll lets me use Markdown. Markdown is super lightweight, easy to learn, and I was already kind of familiar with Markdown because I use GitHub.

### Your Workflow will now be Upgraded
By taking more control over my blog, I am freed up to do cool things.

#### Version Control via git
With Jekyll, I can keep my blog in version control using git. I can create a branch for drafts, and merge them to master when they are complete.

#### Continuous Integration with Travis-CI
I have Travis-CI continuously building my master branch and pushing it to an S3 bucket. Before the build assets get pushed to S3, Travis-CI runs html-proof to make sure all of my links work, and my pages exist.

#### Free SSL and Other Awesomeness from CloudFlare
To serve the site, I am using CloudFlare. CloudFlare lets me serve from an S3 bucket. Then, I can enable a bunch of kickass options such as caching, free SSL, and all sorts of pluggable apps. Integrating Google Analytics at the CloudFlare level was as simple as enabling the app and authorizing CloudFlare with my Analytics account.

CloudFlare gives you three rewrite rules with the free site account and I used those to redirect all of my old domain's traffic over to my new domain. It was incredibly painless.

CloudFlare's free SSL takes 24 hours to enable, so it hasn't been turned on for my domain yet.

#### Disqus for Comments
I had heard of people using Disqus when serving a static site out of an S3 bucket. I didn't expect it to be easy to setup, but to my surprise it was a piece-of-cake*. I exported my posts using the built in WordPress exporter. Then, I had to replace all mentions of my old domain in the XML export with my new domain to ensure that Disqus would match the old comments to the new post address. I uploaded the file to Disqus and it just worked. That's a definite win.

#### Slack Channel for Notifications
I created a Slack channel with Travis-CI and GitHub integration. Now I have a unified, persistent activity log for my blog.
![Slack Notifications][1]


*Cake was not a lie.

[1]: /images/posts/2014/10/slack-notifications-for-blog.png
