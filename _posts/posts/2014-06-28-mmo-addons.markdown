---
layout: post
title:  "Building MMO Addons"
date:   2014-06-28 09:14:15
categories: blog
excerpt: A short web development departure
---

I've always loved tinkering with the user interface whenever a game allows it. I remember modifying ini files in [Tribes](http://en.wikipedia.org/wiki/Tribes_(series)) to move around the health bars so that they were easier to see, and I would toy with addons for hours in [http://en.wikipedia.org/wiki/World_of_Warcraft](World of Warcraft) trying to make the perfect interface. Lately I've been playing [Wildstar](http://en.wikipedia.org/wiki/WildStar_(video_game)), a new MMO that provides a powerful API for making addons. In fact, the stock interface was developed entirely with the public API so an aspiring addon developer can crack open any element of the in-game interface and poke around (which was important since there's no documentation). The Wildstar developers call this [peer-level functionality](https://forums.wildstar-online.com/forums/index.php?/topic/55410-addons-that-display-enemy-units/?p=595084) and it has allowed for a lot of powerful addons like an addon that [cheats for you](http://www.curse.com/ws-addons/wildstar/220323-cheatsimon) or one that [displays huge lines to your enemies](http://www.curse.com/ws-addons/wildstar/220025-track-master).

<p align="center">
  <img src="/images/wildstar-api.png" class="blog-img"/>
  <span class="caption">Browsing the Wildstar API with [Rover](http://www.curse.com/ws-addons/wildstar/220043-rover)</span>
</p>

Unfortunately the Wildstar UI has a lot bugs. In fact, there are dozens of addons dedicated to just fixing one small thing with the stock addons. I discovered one of these bugs during a beta test — the player's selected mount simply wouldn't save  in between sessions. I spent a few hours learning [http://www.lua.org/](Lua), the programming language used in Wildstar's addons, and implemented a quick hack to solve the problem. I shared it with my group of friends and uploaded it to [Curse](http://www.curse.com/ws-addons/wildstar/220412-defaultmount) where it was downloaded thousands of times. I was hooked at this point and wanted to make something more ambitious.

In Wildstar there are "rare" creatures that drop special items or satisfy some sort of in-game achievement when killed. The problem, of course, is finding these creatures in the vast game world. I dug through the API and found that unit information is constantly sent to the game client every few frames. By cross-referencing incoming unit names with those found in the [game achievements](http://wildstar.gamepedia.com/Kill_achievements) I was able to write an addon that detects nearby rares. Thus, [RareTracker](http://www.curse.com/ws-addons/wildstar/220585-raretracker) was born.

<p align="center">
  <img src="/images/raretracker.png" class="blog-img"/>
  <span class="caption">Tracking rares!</span>
</p>

RareTracker ended up being my most popular addon with over 150,000 downloads as of writing this post. I don't work on it much anymore but I spent as much time developing RareTracker and other addons as I did playing the game itself. Though it was sometimes a lot of effort to provide support and grant feature requests, it was very rewarding to work on something that you personally find useful while also providing it to others. Not to mention a great opportunity to learn a new language!