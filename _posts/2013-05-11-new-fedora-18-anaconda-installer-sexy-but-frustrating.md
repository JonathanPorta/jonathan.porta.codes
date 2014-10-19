---
title: 'New Fedora 18 Anaconda  Installer &#8211; Sexy but Frustrating'
author: Jonathan
layout: post
permalink: /2013/05/11/new-fedora-18-anaconda-installer-sexy-but-frustrating/
categories:
  - Development
  - Fedora 18
  - Linux
---
<div id="attachment_183" class="wp-caption aligncenter" style="width: 596px">
  <img class=" wp-image-183  " title="Fedora 18 Anaconda Installation Summary Screenshot" src="/images/posts/2013/05/Screenshot-from-2013-05-11-2138271-e1368833038132.png" alt="Fedora 18 Anaconda Installation Summary Screenshot" width="586" height="211" /><p class="wp-caption-text">
    Fedora 18 Anaconda Installation Summary Screenshot
  </p>
</div>

The new Fedora installer, Anaconda, looks beautiful. Unfortunately, I wasted a lot of time trying to figure out how to do something I expected to be commonplace. Here&#8217;s how it went down.

## Existing Configuration

*   Dual boot with Windows 7 and Fedora 15.
*   2TB HDD configured with NTFS partitions for Windows, an ext4 boot partition and LVM2 volume group for F15 &#8211; 3 LVs &#8211; home, swap and root.

## What I Wanted to Do

Preserve my /home lv and my ntfs partitions.  Nuke everything else and install Fedora 18.  Pretty straightforward, right?

## The First Hurdle

The first several screens were what you might expect &#8211; time zone, keyboard, nice splash screen.  By the time you arrive on the &#8220;Installation Summary&#8221; screen, pictured above, you are probably enjoying the experience-the aesthetics are pleasing.  It just feels good.

And then *it* happened&#8230;

After clicking &#8220;Installation Destination&#8221; to presumably to setup my partitions, I get this dialog box:

<div id="attachment_177" class="wp-caption aligncenter" style="width: 631px">
  <img class="size-full wp-image-177" title="Fedora 18 Anaconda - Confusing Partition Dialog" src="/images/posts/2013/05/Screenshot-from-2013-05-11-213918.png" alt="" width="621" height="400" /><p class="wp-caption-text">
    Huh?
  </p>
</div>

### My Beef With this Dialog

*   First off, why in the hell would you ever layout information about a hard drive&#8217;s size/space/partitions in a paragraph? That is tabular data, best represented in a clear, no frills grid.  Some data presentation is better left cut, dry and to the point.
*   The first thing I read: &#8220;3.15 GB of available space.&#8221; Great, it thinks I have enough space, even though that number is totally wrong, I have 100s of free GBs available. Whatever. Moving on. Still mentally off frolicking in &#8220;PreTTyNewOS Install Land™&#8221;.
*   The second thing I read: &#8220;1.05 MB Free space available for use.&#8221; Wait, what? \*eyes dart back up to read the first line\*  Oh, I guess I misread that. It NEEDS 3.15 GBs to install.
*   I continue on&#8230;eyes jump back down to &#8220;29.17 GB Free space unavailable but reclaimable&#8230;&#8221; Whatever that means&#8230;
*   &#8220;1.9 TB Space in selected disks reclaimable by deleting existing partitions.&#8221; And by that it means &#8220;Your HDD is 1.9TB&#8221; Of all of the important variables to consider when installing a new OS, the one I seldom care about is hardware, given that at this stage in the process, I would have already made any necessary hardware modifications, such as installing a new HDD. So really, this should not be **bolded** and grouped in such a way that it appears to be of the same level of significance as an incredibly more important piece of information such as &#8220;you do not have enough HDD space, please fix this&#8221;.

&#8220;You do not have enough HDD space available.&#8221;  That is all I needed that dialog to tell me.  Forget the rest of it. Whew! Now that I understand what it is trying to tell me, what are my options?

*   &#8220;Cancel & add more disks&#8221; &#8211; Odd.  I am not sure what this &#8220;upgraded&#8221; cancel button will do if I were to click it.  Surely it must be more than just a standard cancel button, otherwise it would simply say &#8220;cancel&#8221;, right?  Will it back me out of the installation, shutdown my PC and hand me a screwdriver?  Because, that is the functionality I have come to expect out of all the other &#8220;Cancel & add more disks&#8221; buttons out there.  Precedent, yo.
*   &#8220;Modify software selection&#8221; &#8211; This is disabled regardless of what I do, so I guess it doesn&#8217;t want me to do that&#8230;
*   &#8220;Reclaim space&#8221; &#8211; Uh, last time this dialog box had the word &#8220;reclaimable&#8221;, you know,  up there a few lines, it was followed by the phrase &#8220;by deleting existing partitions&#8221; so this button probably means &#8220;Format HDD-Lose all stuffs&#8230;&#8221; There is no way I am ever clicking that button. Why is it even there? Did someone really put an &#8220;auto-screw-with-my-partitions&#8221; button on this dialog box?
*   At this point I am getting desperate.  I have lost the happy-go-install feelings of late.  I have scanned the important looking items on this dialog, and then looked at my two actionable options. Nothing seems like a clear choice. I am starting to lose faith in this dialog box&#8217;s ability to meet my installation needs.
*   Suddenly, when hope had all but been lost, I see: &#8220;I don&#8217;t need help; let me customize disk partitioning&#8230;&#8221; Now, that is my kind of checkbox! I quickly check the box and prepare to move onto managing my partitions!
*   Are you kidding me? The result of that checkbox was greying out the &#8220;Cancel & add more disks&#8221; button, leaving me alone in the room with what I am perceiving will, once clicked, send the grim reaper of data destruction after my precious bits. No! Bits! I love you!

<div>
  At this point, I am thinking about that backup I didn&#8217;t make and how I probably shouldn&#8217;t have been so lazy&#8230; I should probably press the hard reset button on my PC and just forget about installing Fedora 18 for now.
</div>

<div id="attachment_184" class="wp-caption aligncenter" style="width: 637px">
  <img class="size-full wp-image-184" title="Scariest Button Click of my Life" src="/images/posts/2013/05/fedora-18-installation.png" alt="Scariest Button Click of my Life" width="627" height="409" /><p class="wp-caption-text">
    I sat here for a good 5 minutes wondering if I should click this button.
  </p>
</div>

Finally, I decide to dive in and live a  little. Nothing like a little data loss to go with your freshly installed OS. Reminds me of Windows!  I click it. Success! I am brought to a  screen that looks like a partition manager. I didn&#8217;t screenshot this part because I didn&#8217;t think I would need it, seeing as it should have been trivial from this part forward.

In the left-most column are three headings: &#8220;New Fedora 18 Installation&#8221;, &#8220;Fedora Linux 15 for x86_64&#8243; and &#8220;Unknown&#8221;.  The last is my Win7 installation and the other two are exactly what they sound like. Now, my home partition is under the Fedora 15 header, so I try moving it to the Fedora 18 header. No luck. I continue to mess with the settings until I finally result to googling for an answer. On a page I can no longer seem to find(I wanted to credit it with a link), at the bottom, I discover an incredibly helpful, yet obscure comment that helps me figure out how to use this screen.

## The Secret

*Prepare for a &#8220;derp&#8221; moment*&#8230; Type the mount point into the &#8220;Mount Point&#8221; field. The partition will then place itself under the &#8220;New Fedora 18 Installation&#8221; header.

Yep, that easy. I couldn&#8217;t believe I didn&#8217;t try that&#8230;

To nuke a partition, select the partition on the left.  Enter the mount point, if you have not already.  Then, expand &#8220;Customize&#8221;.  Check &#8220;Reformat&#8221; and verify that the volume group is correct.

<div id="attachment_182" class="wp-caption aligncenter" style="width: 660px">
  <img class="size-full wp-image-182" title="Fedora 18 Installation Partition Manage Screenshot" src="/images/posts/2013/05/Screenshot-from-2013-05-11-213301-e1368836509885.png" alt="Fedora 18 Installation Partition Manage Screenshot" width="650" height="225" /><p class="wp-caption-text">
    Showing the partitions to be reformatted now appearing under the Fedora 18 header.
  </p>
</div>

<div id="attachment_174" class="wp-caption aligncenter" style="width: 660px">
  <img class="size-full wp-image-174" title="Fedora 18 Anaconda Installation  - Moving Old Partitions into new Installation" src="/images/posts/2013/05/Screenshot-from-2013-05-11-215201-e1368836659642.png" alt="Fedora 18 Anaconda Installation  - Moving Old Partitions into new Installation" width="650" height="223" /><p class="wp-caption-text">
    Yay! My /home is under the correct header!
  </p>
</div>

## Installation Complete!

Once the partitions were under the correct headers with the correct mount points and volume group selected, it really was smoother sailing. I left to run an errand, and when I came back Fedora 18 was waiting for me, along with all of my precious bits. I missed you guys!

In all seriousness, I think that the issues, thoughts, and feelings I described above, albeit somewhat melodramatically, could be combined to form the antithesis of the good user experience.  I think this is also a great example of how designers and developers have to be diligent about carrying through good UI practices through every part of every workflow in a program.

What do you think? Did you find this helpful? Please share your thoughts in the comments below.
