---
layout: post
title:  "Wreckfest Mobile"
thumbnail: "/assets/img/wreckfest_mobile/cover.png"
date:   2025-10-22 16:59:24 +0200
releasedate: Nov 15, 2022
categories: project professional
website: https://handy-games.com/en/games/wreckfest/
websitegoogle: https://play.google.com/store/apps/details?id=com.hg.wreckfest&hl=en
websiteapple: https://apps.apple.com/us/app/wreckfest/id1592505377
tools:  [Custom Engine(C++), Visual Studio, Perforce, Jira/Confluence]
permalink: "/:title/"
#imgpath: "/assets/img/wreckfest_mobile/"
videopath: "/assets/video/TitanQuestLegendaryEdition.mp4"
professional: true
---
After porting Titan Quest we started on getting Wreckfest to mobile devices, Android and iOS.

We had access to all of the PC versions sources and due to it being a much more modern game(and engine) had fewer problems to deal with.
Bugbear Entertainment(the original developers) were working on a Google Stadia build during that time and implemented a Vulkan renderer for that, which we could use as well without needing major changes.

I initially worked on getting the game to run at all on Android and later worked on adjusting the UI and asset build pipeline.

We implemented SDL 2 to use for window and Input handling and I fixed the Vulkan renderer to run on Android devices(which mostly was changing the used image formats to supported versions), as well as implementing the ASTC encoder(https://github.com/ARM-software/astc-encoder) into the existing toolchains.

Afterwards I focused on adjusting the UI for touch devices(the game did not use buttons for everything, many interactions were based on button/key inputs).
This included initial support for controllers as well.
We also made an effort to have the mobile version of the game run as close to similar on a PC as well, meaning it used a similar screen(aka window) size and used the mobile UI instead of the PC UI, all to ease testing, development and debugging.

It was discussed if we also implemented support for online matches, with servers run by our company, but this was discarded mostly for cost reasons, we were not sure if they would have been worth it.
But I implemented a basic implementation for LAN multiplayer, so players could play together in the same Wifi.
The game/engine supports multiple multiplayer/network drivers but not local multiplayer implementation, but at least I had an interface I could follow.

Lastly I integrated support for the Google Play Store, handling asset and DLC management.

I left the company a few months before release.
