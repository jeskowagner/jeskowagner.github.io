---
layout: page
title: Scraping housing offers
description: "Or: how I got my current apartment"
img: assets/img/house.png
importance: 4
category: other
---

| Language      | Python                                       |
| Further links | [https://git.io/Jz01H](https://git.io/Jz01H) |
|               |                                              |

Like many cities, Edinburgh has a housing problem. Families sometimes wait [three years](https://www.edinburghlive.co.uk/news/edinburgh-news/housing-crisis-shocking-figures-show-19151056) for a suitable flat.
To tackle housing issues, the University of Edinburgh [guarantees accommodation to postgraduates](https://www.accom.ed.ac.uk/applying/guarantees/).
However, it is often more expensive (can be ~800£/m) and cannot accommodate students not moving alone.
Heaps of students are therefore trying their luck on the private market, which further renders the market very competitive. 

In this pet project, I wanted to make the search for accommodation a little easier to improve chances of finding a suitable apartment.
Specifically, I was looking to cut down on the overhead of clicking on each individual advert to determine whether it is interesting enough to apply to.
Tens of ads go online every day, and when starting it can be overwhelming to skim through hundreds of offers.
My aim was therefore to scrape housing offers, filter them based on my chosen criteria, and apply rapidly to interesting offers.
I chose to scrape [Rightmove](https://rightmove.co.uk/) because it is one of the biggest websites to find housing offers.

Since I have no background in web-scraping I read through a few tutorials and got started with [BeautifulSoup](https://pypi.org/project/beautifulsoup4/).
This library makes extracting HTML from pages easy. 
I used it here to first scrape the housing overview for Edinburgh on Rightmove, extracting all links to offers. 
Then, I scraped all offers for information that is interesting to me, like start of rental contract, price, and location. 
I packaged this application in an executable GUI program that I could run a few times a day to generate a pretty Excel sheet. 
All that was left to do then was to look at the 1-2 interesting offers a day and get in touch with the agent. 

And it worked! After a few weeks of writing different agents I found an apartment. By automating the process of scraping the market I saved time and learned a new skill, all the while being able to focus on other aspects of moving country. 
For all those seeking to scrape rightmove in a similar way, check out my GitHub repository [here](https://git.io/Jz01H). 

