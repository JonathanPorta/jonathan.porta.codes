---
layout: post
title:  "Automatically Build your Unity3D Project in the Cloud using TravisCI for free"
date:   2015-03-21
categories:
permalink: /2015/03/21/automatically-build-your-unity3d-project-in-the-cloud-using-travisci-for-free
comments: true
---

Whenever I find myself doing something over and over and over again I usually get frustrated. I am kind of an impatient guy. At least when it comes to software and the process of developing software.

Unity3D's ability to cross-compile your game for tons of platforms is pretty badass. It solves the multiplatform problem very well. But, it stil leaves a lot up to the developer, like, actually making the game (duh!) and getting the finished game asset to the player. Often developers will use some sort of distribution service/platform/store to get their game to the player. But, there are some steps missing. How does one generate builds for testing every single time there is a code change? How does the final product make it to the distribution service? Where do hats come from? (Just seeing if you're still reading or asleep from my boring ranting.) I want to put together a guide, or perhaps a series of guides, that helps new Unity3D game creators some of the basic automation that real software companies use.

Well, let's get started!

### Beginning the Journey
If you want to implement your own version of that I am about to describe you are going to need a few development tools available on your machine and you're going to need free accounts for several online services.

#### Development Tools Needed:
- Unity3D 5.0 Personal Edition (at least)
- git
- an environment that allows you to execute bash scripts - If you're using Linux or OS X then you are good to go. If you are using Windows you will need something like ConEmu and gitBash. You can get away without these, but it will be more difficult since you won't be able to test your work locally. You'll have to push each little change to your GitHub repository and rely on CircleCI's output to see debug.

#### Accounts:
- Github.com - This is one of the most popular online code hosting services. They have definitely earned their popularity by building a great service that helps developers do their job. Plus, it's free if your repository is open to the public, and super cheap if you want to have hidden repositories. There are other places to host a git repository, but for this guide I am only going to cover GitHub.com.
- Travis-CI.org - Travis is a continuous integration service that is super flexible. I've used it to build tons of different project types, run thousands of tests, and even check the status of the Linux Rust multiplayer server. Use your GitHub account to signin and create an account. Travis will need to be able to see your GitHub repositories, so it's easiest to just signup with your GitHub account.

### Overview
- Create a sample unity project, set the project settings to be compatible with git, set the default scene for builds, and finally commit and push your sample project.
- Whip up some scripts that handle building your project.
- Install the TravisCI gem and configure the travis.yml file to use the build scripts we wrote in the previous step.
- Setup S3 Bucket Upload and/or GitHub tagged release.


### TravisCI







 This is the first in that series of guides. I am

But, it's only part of the solution to But, what if it could be even better? What if, instead of requiring me to manually export builds, it could just happen? This question has been rattling around in my brain ever since I built my first Unity3D game a few months ago.

I have always enjoyed building, tweaking, andautomating build pipelines. Deploying things by hand is so 2005, amirite?


[![my_image]][my_image]





[my_image]: /images/posts/2015/03/
