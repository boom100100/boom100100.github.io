---
layout: post
title:      "Trending News Rails/Javascript Final Project"
date:       2020-02-17 15:50:43 +0000
permalink:  trending_news_rails_javascript_final_project
---

Twitter has a massive pool of data consisting of tweets and collections that they have organized by various categories. Even better, Twitter has made that data available to developers in its own API. Various news sites have a comparable dataset, and they have also exposed that data in numerous APIs. The marriage between these two types of resources is the inspiration of my app, Trending News (TN).

TN is a single page app that pulls trends from Twitter and cross-references those trends with The Guardian Api's articles, all in real time. A user of TN may click a button on the GUI index.html page, or make a call directly to the topics and links endpoint to automatically generate trends and articles from the current subset of trends. The end result is a bunch of articles from a reputable source that are related to a specific trend.

*Note: The scope of this project was originally to search numerous news sources, but testing maxed out the number of calls in APIs that could pull articles from different news sources.*

Next steps for this app include figuring out how to make it more efficient. Fulfilling promises for multiple API calls has proven to be painfully slow. It is also necessary to figure out a billing plan that matches likely usage so TN can make unlimited calls to the APIs it depends on. Additionally, an email feature for the GUI that can send links would make a good social component.
