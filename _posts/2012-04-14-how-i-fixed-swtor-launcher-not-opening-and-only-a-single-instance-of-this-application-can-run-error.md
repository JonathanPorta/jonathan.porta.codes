---
title: 'How I fixed SWTOR launcher not opening and &#8220;only a single instance of this application can run&#8221; error'
author: Jonathan
layout: post
permalink: /2012/04/14/how-i-fixed-swtor-launcher-not-opening-and-only-a-single-instance-of-this-application-can-run-error/
categories:
  - Video Gaming
tags:
  - 1.2 Legacy Update
  - 1st World Problems
  - 'Star Wars: The Old Republic'
  - SWTOR
---
Recently I have been playing Star Wars: The Old Republic.  It is the first time I have ever tried an MMORPG.  I am a fan of most everything Star Wars, so, I had to try it out.  Sadly, after playing for a few weeks, I was greeted with this:

[<img class="aligncenter size-full wp-image-20" title="only-single-instance" src="http://jonathanporta.com/wp-content/uploads/2012/04/only-single-instance.png" alt="" width="312" height="144" />][1]

[Skip to the fix&#8230;][2]

Popping open task manager showed that, even though the launcher was not visible on the task bar or anywhere on my screen, the program was indeed running:

[<img class="aligncenter size-full wp-image-12" title="task-manager" src="http://jonathanporta.com/wp-content/uploads/2012/04/task-manager.png" alt="" width="810" height="612" />][3]

&nbsp;

I ended the &#8220;launcher.exe&#8221; process and tried to open the launcher again.  Nothing seemed to happen.  So, I clicked on the launcher a third time.  This time, the same error, &#8220;Only a single instance of this application can run&#8221;. Next, I navigated to the folder containing launcher.exe to see if there were any clues there.  There is a second executable called &#8220;FixLauncher.exe&#8221;.  But, that only resulted in a new error:

[<img class="aligncenter size-full wp-image-17" title="fix-launcher-failed-need-to-close-launcher-process" src="http://jonathanporta.com/wp-content/uploads/2012/04/fix-launcher-failed-need-to-close-launcher-process.png" alt="" width="527" height="392" />][4]

&nbsp;

Since it told me to restart my computer, I assumed this was due to the fact that launcher.exe was running in the background again.  I opened up task manager again, and indeed, launcher.exe was running.  I ended it and ran FixLauncher.exe again.  This time there were no errors but the installed exited without any sort of message.  Then, I tried launcher.exe again.  Still, nothing.  I opened up task manager and closed the launcher.exe process again. At this point, I decided to do some Googling.  I found a post on the SWTOR forum, but it didn&#8217;t help.  It basically suggested to do what I just described doing above.  Not much help.  But, then I found this answer on the Gaming Stack Exchange: <a href="http://gaming.stackexchange.com/a/49716" target="_blank">http://gaming.stackexchange.com/a/49716</a>.  In the answer, Adanion suggests to delete the patch folder.  So, I deleted the patch folder:

[<img class="aligncenter size-full wp-image-13" title="delete-patch-folder" src="http://jonathanporta.com/wp-content/uploads/2012/04/delete-patch-folder.png" alt="" width="798" height="640" />][5]

&nbsp;

Ran FixLauncher.exe again:

[<img class="aligncenter size-full wp-image-15" title="fixing" src="http://jonathanporta.com/wp-content/uploads/2012/04/fixing.png" alt="" width="527" height="392" />][6] **

&nbsp;

<p style="text-align: center;">
  <em>Drum Roll Please&#8230;</em>
</p>

** [<img class="aligncenter size-full wp-image-19" title="launcher-updating-after-fix" src="http://jonathanporta.com/wp-content/uploads/2012/04/launcher-updating-after-fix.png" alt="" width="1000" height="632" />][7]

&nbsp;

Success! After the launcher updated itself, it reopened ready to login.  After logging in, the launcher started downloading the latest game updates and all was right in the world again!

[<img class="aligncenter size-full wp-image-14" title="downloading-remaining-patch-files" src="http://jonathanporta.com/wp-content/uploads/2012/04/downloading-remaining-patch-files.png" alt="" width="1000" height="632" />][8]  
<a name="quickfix"></a>

### TL;DR&#8230;

1.  Open task manager and look for &#8220;launcher.exe&#8221;.  If it is in the process list, kill it.  Be sure it actually dies before moving on.
2.  Open explorer and navigate to &#8220;C:\Program Files (x86)\Electronic Arts\BioWare\Star Wars &#8211; The Old Republic&#8221;.
3.  Delete the &#8220;patch&#8221; folder.
4.  Run &#8220;FixLauncher.exe&#8221;.
5.  Run &#8220;launcher.exe&#8221;.
6.  The launcher will update itself and then you should be able to login and play as normal.

 [1]: http://jonathanporta.com/wp-content/uploads/2012/04/only-single-instance.png
 [2]: #quickfix
 [3]: http://jonathanporta.com/wp-content/uploads/2012/04/task-manager.png
 [4]: http://jonathanporta.com/wp-content/uploads/2012/04/fix-launcher-failed-need-to-close-launcher-process.png
 [5]: http://jonathanporta.com/wp-content/uploads/2012/04/delete-patch-folder.png
 [6]: http://jonathanporta.com/wp-content/uploads/2012/04/fixing.png
 [7]: http://jonathanporta.com/wp-content/uploads/2012/04/launcher-updating-after-fix.png
 [8]: http://jonathanporta.com/wp-content/uploads/2012/04/downloading-remaining-patch-files.png