---
title: "6 weeks of building my dream with Buildspace Nights & Weekends"
datePublished: Wed Jun 14 2023 00:05:50 GMT+0000 (Coordinated Universal Time)
cuid: cliuybdac000b09jmeo3o2u4n
slug: 6-weeks-of-building-my-dream-with-buildspace-nights-weekends
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1686698398738/275214d3-b95b-4119-8aef-5d4fb98dfd93.jpeg
tags: build, innovation, buildingandlearning

---

Six weeks ago, I got accepted into [Buildspace's Nights & Weekends program](https://buildspace.so/) with just an idea. A website to learn languages through songs. I've never built a product for users, but I figured that after learning programming since 8th grade, now is the time! Keep reading to see how I built [Songlingo](http://song-lingo.com)!

Nights & Weekends is a free, six-week, program that is geared towards people who are either working or studying full-time during the week and are excited to devote six weeks of their spare time to advance an idea that they have.

In the beginning, participants pick a goal for the six weeks. My goal was to reach 500+ unique users on Songlingo.

For more information about Buildspace, and their recently raised $10 million from Andreessen Horowitz and other investors like Founders Inc and Y-Combinator, check out [this article](https://techhubsouthflorida.org/former-south-floridian-farza-majeed-raised-10m-backed-by-andreesseen-horowitz-now-helping-others-ideas-come-to-life/) I wrote for the South Florida Tech Hub.

These six weeks have been the busiest, but best six weeks of my life. With the second semester of Junior year of high school, four AP tests, and multiple trips, it's been a great ride!

## Week-by-week progress

### Week 1

I was in Boston and New York during the first week visiting family and touring colleges. I watched the Buildspace kickoff live stream in the car on the way back from a college tour. I finalized my idea by Thursday, April 13, and then, Farza, the founder of Buildspace, said that by Sunday, we should have version one of our idea! That got me building, and I started my React project in the car from Boston to New York. I built my v1, which could only fetch a song's lyrics and music video, no translation yet. But that was enough to submit for the first weekly update!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686699007679/0a31671d-6505-4f2d-8ebd-45ad9b668d07.jpeg align="center")

### Week 2

After that, I really got to work for the second week. I added the translation functionality for one word, using langchain and ChatGPT API originally, but then switched to Bing Translate API and then Google Translate API. I also researched analytics services, and decided on [Posthog](https://posthog.com/), which offers useful features like session replays.

I switched Songlingo to be a Next.js website, from React, which allowed me to call APIs and run server-side functions.

I launched Songlingo on Twitter for the first time on April 24, and got my first user! He helped me realize that the Youtube data API has a very low rate limit, which was causing an error after a few searches. I had to switch it up.

### Week 3

I decided on a free NPM package, which allows you to search for a Youtube video and fetch its ID. With this, I embedded an Iframe with the music video and audio into Songlingo.

I then added the full song translation, which was helpful for users.

### Week 4

I booked my flight and hotel for the San Francisco in-person Nights & Weekends event!

I added translation to any language, so a song in Spanish could be translated to a song in French, with no English involved anymore! I fixed the reverse formatting of right-to-left languages to make them readable, and then tweeted about both of these features.

I then got feedback that it was hard to read lyrics without line separation by verse, so I reformatted the lyrics and added spacing.

![Screenshot from Jazzify](https://pbs.twimg.com/media/FvVOzpNXwAAtY8L?format=jpg&name=900x900 align="left")

I then bought the domain [song-lingo.com](http://song-lingo.com), and started spreading the word. I told my language teacher about it, and she used Songlingo during our class to play a song and show the translation! The whole class really liked it!

I added social media share buttons, so users can share which song they are learning!

### Week 5

I had an engineering field trip to the Drones in School national competition at the AUVSI XPONENTIAL conference. On the plane, I redesigned Songlingo and made a logo.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686699241936/7ceef34d-0b03-4fcc-a535-5b7fc758b937.jpeg align="center")

I then learned that some users didn't know which song to enter, so they left the website. I added a feature that allows users to retrieve a random song in any language, in case they want to explore new songs!

### Week 6

I posted Songlingo in over 30 language subreddits, like r/Korean, r/Vietnamese, r/Spanish, r/Italian and many more. I then watched Posthog analytics, and watched it take off. Within two days, Songlingo broke through my goal of 500+ users, and had 1,500 unique people open the website!

I then added URL params and destructuring, so users can share the link to a specific song.

*For more weekly progress, check out* [*my Twitter*](https://twitter.com/adamcandoit)*.*

## Demo Day

After week 6, we had demo day and the final 32, where we voted on who wins $100,000. It was amazing to see other projects.

![Final-32 live stream to vote who wins $100,000](https://cdn.hashnode.com/res/hashnode/image/upload/v1686695917897/d316fa13-b2a6-4434-962d-8eb4d1ae152c.png align="center")

## IRL (In real life) event

I flew to San Francisco for the Buildspace in-person event, three incredible days of meeting over 250 other builders and improving Songlingo! The energy in the room was amazing, with everyone checking out each others' projects and helping each other! It was inspiring to meet the builders who I'd been building with side by side for 6 weeks!

![Buildspace school in San Francisco](https://cdn.hashnode.com/res/hashnode/image/upload/v1686696575888/d6f614c1-73c2-4920-98bf-8d0bdec182d6.jpeg align="center")

At night, I went back to the hotel and worked with [Rox](https://twitter.com/RoxCodes) and [Aprilynne](https://twitter.com/AprilynneAlter) on our individual projects until 1:30 AM. I started a [newsletter](https://songlingo.beehiiv.com/subscribe) so users can sign-up for updates.

I launched Songlingo on ProductHunt, with the help of [Dylan Molina](https://twitter.com/dxlantxch), which got over 90 upvotes, top 15 product of the day, and number 2 education product of the week!

[Tylar Campbell](https://twitter.com/StoneAgeTc) helped me record a social media video, which drove a lot of traffic to the ProductHunt post.

The IRL event in San Francisco was great! They had plenty of opportunities to get feedback and improve our products. They hosted an insightful question-and-answer session. And they had great food!

![Farza addressing the builders at the San Francisco in person event](https://cdn.hashnode.com/res/hashnode/image/upload/v1685288049591/0f06ebf6-e0cd-430b-a3f1-46ac889be2ce.jpeg align="left")

## After Buildspace

I added Supabase as a database, as well as authentication so users can sign-up, and save words and songs to listen to later!

In order to improve the site performance, I moved the fetch lyrics function to the server side, and I plan on moving other elements as well.  
  
I improved the UI of Songlingo, added [Tailwind CSS](https://tailwindcss.com/), and made the buttons more responsive.

## Recap

It's been an amazing six weeks, going from nothing to a full product with users. I've never done this before, and I'm so thankful to Buildspace for giving me the opportunity and environment to build.

For years, I've said that I will make a big website or app eventually. Maybe in a year. But I never thought I'd actually do it now, and with Buildspace, it was possible.

Before Buildspace, I was stuck in this cycle of learning HTML, CSS, and JS without React JS, because I thought I wasn't ready for frameworks. But after a few weeks of learning React and Next.js through practice, they are no longer a challenge, both came naturally.

I'd highly recommend Buildspace to anyone, whether you have never built anything before, or whether you are a seasoned builder.

Nights & Weekends Season four starts on July 1. [Apply here](http://buildspace.so)!