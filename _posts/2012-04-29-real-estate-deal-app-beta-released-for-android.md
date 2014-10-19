---
title: Real Estate Deal App Beta Released for Android
author: Jonathan
layout: post
permalink: /2012/04/29/real-estate-deal-app-beta-released-for-android/
categories:
  - Android
  - Real Estate
---
&nbsp;

I spent a couple hours today figuring out how to sign and release my first Android Market &#8211; yes I know it is now called &#8220;Play!&#8221; &#8211; app.  I have written quite a few Android apps over the last two years, but, oddly, none that I have personally published.  So, here is my debut with a very simple app.

[<img class="aligncenter size-full wp-image-51" title="Real Deal - Maximum Offer" src="/images/posts/2012/04/device-2012-04-29-193008.png" alt="Screenshot" width="480" height="800" />][1]

When I realized I was performing the same simple calculations over and over I decided I needed an app to handle that for me.  Hence Real Deal was born.  The app is very simple, but has some potential.

<a title="Find Real Deal on Google Play!" href="http://play.google.com/store/apps/details?id=org.smartinvestments.realdeal" target="_blank"><img class="aligncenter" src="http://www.android.com/images/brand/get_it_on_play_logo_large.png" alt="Get it on Google Play" /></a>

The app uses the following metrics:

*   **After Repair Value** &#8211; the value of the property if it was &#8220;squeaky clean&#8221; and &#8220;brand new&#8221;.
*   **Repair Estimate** &#8211; a spinner of potential repair values.  The spinner&#8217;s lack of precision is intentional.  Select the number that your estimated repair costs fit within.  For example, if you think there are about $16,000 of needed repairs, select $25,000.  If it costs less, great!
*   **Target Position** &#8211; what ratio of investment to value do you want to be at when done with the project.  By default it is set to 65%.  Generally if you are only 65% into a property, you should have no issues selling it quickly.

<div>
  The output is the maximum offer that should be made on the property based on the data you entered.  The calculation is very simple:
</div>

<div style="text-align: center;">
  (After Repair Value &#8211; Repair Estimate) * Target Position
</div>

<div style="text-align: left;">
  I have some ideas to add, time-permitting, but if you have any ideas or comments leave them below!
</div>

 [1]: /images/posts/2012/04/device-2012-04-29-193008.png
