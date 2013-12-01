---
layout: post
title:  "Tracking eSports"
date:   2013-09-01 08:20:25
categories: blog
excerpt: Part 2 - Features
---

In my [last post](/blog/tracking-esports-part-1/) I introduced eSports Tracker as a tool for keeping up-to-date with the latest eSports events. In this post I'll talk more about the roadmap for eSports Tracker and some of the other features I'm excited to work on.

The first goal of eSports Tracker is to provide a single, clean page that tells you everything you need to know for the current week. If you don't follow competitive sports you may not realize this already exists for things like the NFL, NBA, and MLB. As I'm writing this post the NFL season is underway. Try googling ["nfl schedule"](https://www.google.com/search?q=nfl+schedule) to see what I mean:

<p align="center">
  <img src="/images/nfl-schedule.png" class="blog-img"/>
  <span class="caption">Search results for "nfl schedule"</span>
</p>

I don't even have to click on a search result to find the information I'm looking for. On top of that, the very first result is exactly what I wanted in the first place. This is the kind of tool I want for eSports and the primary motivation behind this project. As soon as I can glance at a page and know within a matter of seconds what I'm going to watch in the next few days I'll know I'm on the right track.

I'm also interested in 'big picture' stats. There are [great](http://dotabuff.com/) [websites](http://www.lolking.net/) that track detailed statistics about hero picks, matchup stats, item trends, and much more. These 'micro' statistics are interesting in the short term but have little utility several months after the fact. I want to track statistics like average prize pools, number of tournaments, and tournament regions. Combined with temporal data, I want to be able to track the relative health of competitive games. For example, the amount of money earned in Dota 2 vs. League of Legends in the past 3 months or total SC2 prizes earned in Korea vs. North America. Given only a few different statistics, we can see how games are trending over time and we can compare games to each other.

Another problem I'd like to tackle is the promotion of smaller games. As I mentioned in part 1, the only central place to find tournament streams is Twitch.tv, but their interface favors games that are already popular. For example, there's a big Super Smash Bros. Melee tournament happening as I write this (the "world's largest" according to the stream) but only 1200 people are watching it making it the 17th most popular game on Twitch. If I hadn't been exploring the bottom half of Twitch's streams page I wouldn't have known that one of the biggest competitive events for an interesting game that is happening right now. With the data that eSports Tracker collects, we will have the ability to promote small games that are having their big events since we'll be able to analyze statistics like prize pool variance and the number of events per year. For example, if SSB:M has several $250 prize pool tournaments, and only one $5,000 prize pool tournament, we can assume that is a pretty big event for them and notify our users that an interesting tournament is currently going on that they might want to watch.

In the next post I'll talk about some of the challenges so far in implementing eSports tracker such as API integration, leveraging user input, and designing a clean interface that provides an awesome user experience. 
