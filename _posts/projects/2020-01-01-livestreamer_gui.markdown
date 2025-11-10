---
layout: post
title:  "Livestreamer GUI"
thumbnail: "/assets/img/livestreamer/cover.png"
date:   2025-10-22 16:59:24 +0200
categories: project private
tools:  [Jave, Eclipse]
permalink: "/:title/"
imgpath: "/assets/img/livestreamer/"
personal: true
---
<b>Note: This application most likely will not work at the moment, I have not updated it in several years and the Twich API most likely changed in the meantime.</b>

This application is a GUI for the console applications livestreamer and streamlink. These applications allow the viewing or recording of supported streaming services on external video players (like the VLC player).
It provides an easier access to these applications API and provides several other functions, mostly focused around the streaming service of Twitch.tv.
I created this small application because there were no other GUI application which fit my needs at the time. It also was an opportunity for me to deepen my knowledge of the Java language(Java 7 and 8).

The application is written entirely in Java,using the JavaFX framework for all the GUI, with the exception of some css files used for styling.
Used tools were Eclipse, git and Gradle. I used a standard git branching workflow.
Together with Gradle and some plugins I can create a working executable with a single Gradle command.


General Feature Overview
- Management for multiple list of channels for separate streaming sites
- 2 GUI Skins (light and dark)
- Dropdown to choose stream quality
- Usable with either the livestreamer or the streamlink application

Twitch.tv special feature overview
- Continuous checking of online status of each channel
- Download of preview image and meta data of online channels
- Popup Notifications plus alert settings for channels coming online
- Several buttons for quick actions: Start playback or record via livestreamer/streamlink, open in-built chat client or open the official chat in a browser window, open the channel in a browser window
- Import favorite channels for a given username
- Simple internal browser for all twitch.tv channels, sorted by channel category
