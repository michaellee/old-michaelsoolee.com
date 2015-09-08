---
layout: post
title: "Adobe Creative Cloud stuck on Mac and how to fix it"
category: "work"
link: "https://forums.adobe.com/thread/1338906"
date: 2015-09-08 13:34:00
---

Adobe Creative Cloud has been sitting in my menu bar for a while letting me know that I had updates. Problem was, every time I would open the Creative Cloud app to update my apps, it would just hang there, stuck and show a blue spinning wheel. After doing a quick search online, I found the [solution to the problem on the Adobe forums](https://forums.adobe.com/thread/1338906).

> Open Finder, click on Go > Go to Folder. Type in ~/library and hit enter.
>
> Open Application Support/Adobe folder and rename OOBE folder to OOBEold.
>
> Click on Apple icon on the top left, select System Preferences
>
> Choose the network that is currently connected to internet that can be Ethernet or Airport(Wireless). Click on Advanced button and click Proxies Tab.
>
> Under 'Select a Proxy server to Configure' Uncheck all the proxy check boxes, then uncheck 'Use Passive FTP Mode (PASV)'.
