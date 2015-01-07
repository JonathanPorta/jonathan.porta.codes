---
layout: post
title:  "BLOKr 1.2 Update Released"
date:   2015-01-04
categories: development games Unity3D android ios
permalink: /2015/01/04/blokr-1-2-update-released
comments: true
---

[![start_screenshot]][start_screenshot]

A [while back][blokr_post] I released my first Unity3D game for iOS and Android. The original version had very basic gameplay and graphics, so I thought it would be fun to revamp the color scheme and add a few things to make the gameplay a little better.

### Color all the things!
I really like the white on red icon, so I decided rebuild the game's scene based on the high contrast, white on red depicted in the app icon.

#### App Store Preview
<iframe width="740" height="450" src="//www.youtube.com/embed/y8hpQ8hVUcA" frameborder="0" allowfullscreen></iframe>

#### Screenshots
[![in_game_screenshot]][in_game_screenshot]

[![game_over_screenshot]][game_over_screenshot]

### Gameplay updates
Originally, there was no limit to the speed or acceleration that you could obtain so after a while your jumpy block character(yes, it might not have a face but it's still a character! Ok, maybe not.) would be flying from one side of the screen to the other faster than one could hope to control it. I implemented a velocity cap to keep the speed manageable.

I've also added support for the iOS gamecenter and setup a leaderboard. And, of course, fixed some annoying bugs.

I am pretty happy with the game. It isn't much, but it is the first mobile game that I've worked on. I found it to be fun and a good break from the day-to-day programming problems that I get to solve. Plus, Unity3D was very easy to pickup and get started. And, when I did get stuck, there are tons of tutorials, blog posts, and forums with example code and people willing to help.

Check out the [original post][blokr_post], or play BLOKr on your iOS or Android device:

Play Store | App Store
------------------|----------------
[![Get it on Google Play][play-badge]][1] | [![Get it on App Store][apple-badge]][2]

[start_screenshot]: /images/posts/2015/01/blokr-1-2-start-screenshot-ios.png
[in_game_screenshot]: /images/posts/2015/01/blokr-1-2-in-game-screenshot-ios.png
[game_over_screenshot]: /images/posts/2015/01/blokr-1-2-game-over-screenshot-ios.png

[blokr_post]: /2014/10/01/thoughts-after-publishing-my-first-unity3d-game-on-the-apple-app-store-and-google-play-store/

[apple-badge]: /images/badges/apple.svg
[play-badge]: /images/badges/google-play.png

[1]: https://play.google.com/store/apps/details?id=com.jonathanporta.blokr
[2]: https://itunes.apple.com/us/app/blokr/id918951183
