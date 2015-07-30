---
layout: post
title:  "Don't want to wait for the Windows 10 rollout? Trigger the Windows 10 update manually!"
date:   2015-07-30
categories:
permalink: /2015/07/30/don-t-want-to-wait-for-the-windows-10-rollout-trigger-the-windows-10-update-manually-
comments: true
---

Impatient? Me too. I found a way to skip waiting for the Windows 10 upgrade to roll it's way onto your machine and force an upgrade right now.

> I wrote this post because a bunch of [other methods of forcing the upgrade](#failed-alternatives) didn't work for me.

## tl;wr?
Here's the no BS version for power users:

  1. Download [Windows 10 Media Creation Tool page][media_creation_tool_download]
  2. Run Media Creation Tool and choose the "Upgrade this PC" option on the first screen.
  3. Keep advancing steps in the wizard until the installation begins.
  4. Profit.

## The Nice Long Version
I found a quick and simple way to force the Windows 10 update to install on your PC so that you don't have to wait for the rollout to reach your machine. Here are the steps I took to upgrade my PC from Windows 8.1 to Windows 10 earlier today.

# 0. Run the update pre-check
Windows 7, 8 and 8.1 have a pre-update utility that make sure that your PC won't run into incompatibility issues when updating. It's available by clicking that Windows 10 icon on your task bar. (You know, the one that showed up unexpectedly a couple of weeks ago and has yet to leave.)

So that you know what you are getting yourself into, it's probably a good idea to run this before you try to upgrade. If the output is agreeable, then move onto the next step.

> I think the Media Creation Tool does this check for you as part of the upgrade process. So, this step might not be needed.

# 1. Keep Calm and Download Microsoft's Media Creation Tool
Don't worry, we don't actually need to make any "installation media". The media creation tool has a built in update feature that lets you download and launch the update right from Windows.

From a PC running Windows, visit the [Windows 10 Media Creation Tool page][media_creation_tool_download] and download the 64 or 32 bit version, depending on your system.

> I noticed that if you follow the link above on an OS other than Windows you get redirected to the [ISO download page][iso_download]. While you could use the ISO to install, it will require a way to burn or mount the ISO and will take longer than using the media creation tool.

# 2. Run the Media Creation Tool
When you run the Media Creation Tool you should be presented with two options: "Upgrade this PC", or "Create installation media". Make sure the "Upgrade this PC" options is selected and click "Next".

[![step-1]][step-1]

# 3. Wait for installation files to download
The Media Creation Tool should begin downloading the Windows 10 installation files. Wait for it to finish.

[![step-2]][step-2]

> Feel free to keep using your PC.

# 4. Keep waiting
[![step-3]][step-3]

> Is a sandwhich one of those things you are getting ready? I am pretty hungry.

# 5. Accept the License Agreement
[![step-4]][step-4]

> Or not. Consult legal advice if you feel you need it. I am not an attorney and I am not giving legal advice. You might want to read the agreement before deciding. If you do read it, you might be the first person to ever read the Windows 10 license agreement. Go you!

# 6. Wait some more...
[![step-5]][step-5]

> This could be a great time to leave me a comment or catch up on your underwater basket weaving.(It's starting to look abandoned.)

# 7. Wait: The Sequel - in theaters now!
[![step-6]][step-6]

> Ladies and Gentlemen, we'll be pulling back from the gate as soon as the pilot finishes their final pre-flight checks.

# 8. Wake up! It's ready!
To start the installation click "Next".

If you want to nuke your personal files and apps before upgrading, click the "Change what to keep" text.

[![step-7]][step-7]

Keep some stuff, keep some other stuff or keep no stuff. The choice is yours. Once you've decided whether or not to nuke your data, hit "Next."

[![step-7-option]][step-7-option]

The installer should now begin upgrading your PC to Windows 10. The rest of the installation will run without requiring you to click any more "Next" buttons.

[![step-8]][step-8]

Once installation is complete you'll see a customize screen that lets you customize some settings. Be careful of the weird privacy default settings hidden in the "Advanced" dialog.


## <a name='failed-alternatives'></a>Alternative ways to force the upgrade early
I came across a handful of [forum posts][forum-1] with some users reporting success with several different upgrade options.

I wasn't able to get any of methods I tried to work.

I finally decided to give up and just burn an install disc. I grabbed the Media Creation Tool and it turns out that it is also an upgrade tool. Booyeah!

# Why is the upgrade listed as a failed update?
After poking around the Windows Update UI I noticed that there was an entry for "Upgrade to Windows 10 Pro" in the update history.

I tried restarting and removed the Windows Update cache, but I was unable to get the upgrade to trigger. I have no idea why it tried to install in the first place. And I have no idea why the install failed.

[![failed-update]][failed-update]

# Enable Auto-Install for Updates; Force a windows update.
Go to your Windows Update settings and enable two options:
  1. "Give me recommended updates the same way I receive important updates"
  2. "Give me updates for other Microsoft products when I update WIndows"

Open a command prompt as Administrator and run:
`$ wuauclt.exe/updatenow`

This is supposed to make Windows update go fetch some updates, but it didn't seem to work at all for me.

# Kicking the Windows Update Service
Another [post][forum-2] suggested stopping the Windows Update service, removing the download cache, starting the service and then triggering an update from the command line.

**Here is dump of my command ouput:**
<script src="https://gist.github.com/JonathanPorta/001fd6ec328847dca227.js"></script>




[media_creation_tool_download]: http://www.microsoft.com/en-us/software-download/windows10
[iso_download]: http://www.microsoft.com/en-us/software-download/windows10ISO

[step-1]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-1.png
[step-2]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-2.png
[step-3]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-3.png
[step-4]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-4.png
[step-5]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-5.png
[step-6]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-6.png
[step-7]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-7.png
[step-7-option]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-7-choose-what-to-keep.png
[step-8]: /images/posts/2015/07/windows-10-manual-update-media-creation-tool-step-8-smaller.png

[forum-1]: http://forums.windowscentral.com/windows-10-general-discussion/369824-%2A-how-check-force-windows-10-install.html
[forum-2]:http://forums.windowscentral.com/windows-10-general-discussion/369824-2.htm
[failed-update]:/images/posts/2015/07/windows-10-upgrade-listed-as-failed.png
