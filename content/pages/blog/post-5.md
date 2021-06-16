---
title: Leewardslope is Live! Using Forem.
date: '2021-06-13'
author: content/data/team/gordon-norman.yaml
categories:
  - content/data/categories/tutorials.yaml
  - content/data/categories/news.yaml
tags:
  - Leewardslope
  - Forem
image: /images/forem_post.png
image_alt: Post 5 Image
excerpt: >-
  Today, I'm here to share my ideas on creating a community, experiences,
  struggles and overall fun in bring my community live using Forem.
seo:
  title: Amet Nulla Facilisi Morbi Tempus
  description: 'Estne, quaeso, inquam, sitienti in bibendo voluptas'
  extra:
    - name: 'og:type'
      value: article
      keyName: property
    - name: 'og:title'
      value: Amet Nulla Facilisi Morbi Tempus
      keyName: property
    - name: 'og:description'
      value: 'Estne, quaeso, inquam, sitienti in bibendo voluptas'
      keyName: property
    - name: 'og:image'
      value: images/5.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Amet Nulla Facilisi Morbi Tempus
    - name: 'twitter:description'
      value: 'Estne, quaeso, inquam, sitienti in bibendo voluptas'
    - name: 'twitter:image'
      value: images/5.png
      relativeUrl: true
layout: post
---
Today, I'm here to share my ideas on creating a community, experiences, struggles and overall fun in bringing my [community live](https://app.leewardslope.com/) using Forem.


Being a newbie to Ruby, I knew nothing about the code, the infrastructure, and frankly speaking, I thought Ruby on Rails was an advanced version of Ruby programming language. Haha!

I'm entirely new to web development but not to DevOps, so I tried to pick it up with my gut feel. So I forked the code, deployed it in almost every architecture I was familiar with, to name a few; Heroku, VPS-Linux, VPS-Docker, VPS-Capistrano, Hatchbox by GoRails(One of the best), Render, Kubernetes(I regret this), Buddy works, etc.

Nothing is working -\_- in favor of me. I was disappointed, and I turned towards other alternative platforms like Tribe, Circle, Palapa, Mighty Networks; but I still prefer the version of ThePracticalDeveloper(not everyone might be familiar with this term xD).

All of those platforms mentioned above are unique in their way, but Forem is still the best for my community and aspirations. (More about it later, why I only prefer Forem)

## Forem is on the move

Time passed, and I got familiar with Dev and its code; and out of the bloom in August 2020, Dev opened a New instance and named it Forem. I joined it the moment I got to know about it. I was Hyped. I created numerous issues within GitHub and in Forem to learn more.

Now [Leewardslope](https://app.leewardslope.com/) is live using Forem with our defined self-hosting ecosystem. I always dreamt of creating Leewardslope. Leewardslope is a community that helps to improve the standards and reach of Education within India. Yes, it is a big dream. But let me show you the need for empowerment.

## The genesis of Leewardslope

I studied in one of the most prestigious institutions in India; I was among the 0.5% of the competitors to join the Indian Institute of Technology(IIT Guwahati). Unfortunately, the competition was so high that not everyone could afford the coaching fees.

This unavailability of access to educational institutes is wrong. Education is not a premium product to buy; if one desire to educate oneself, he/she should be capable of doing it. I'm not advocating against the competition-based system, but the numbers are not fair. Only 0.5%(10,000 students out of 20,00,000 competitors every year). At least we should provide them with an alternative way to fill the skill gap.

I cannot teach for more than three hours or visit more than two different places in one day. So how do I solve this issue?

## How can I help people like me?

Many teachers and educators all over my country share my enthusiasm, but they lack a platform. Instead, they rely on social media groups, telegram channels, google drives. All of their efforts are going in the vein of isolating themselves.

That is when Forem showed me a path to help educators bring online to share their content effectively. So, I decided and dedicated myself to create a platform leaving the exploration of educators to my team. "It is a long journey, so we have sufficient time; after all, we are a bunch of college graduates."

Today we have 23 educators to contribute to us; they are still not familiar with the MDX editor but will get the hang of it. We now have a road map and timeline mapped out, and by mid-2022, we might have a clearer view of our path. It is all Thanks to Forem.

## How we are hosting our Forem

Many people over here are more interested in talking about hosting their community than about their community. This is not a criticism; after all, forem.dev is for helping you host your Forem instance.

Ok, let's come to the point. First, I created two digital ocean droplets, one being a dB droplet with backup features enabled, and the other is a forem droplet without any backup. Then, I installed Caprover in my dB droplet while dokku in my forem droplet. Before moving any further, I would like to explain these choices in detail.

Firstly, I don't want to host my Forem in Heroku. It is so expensive if you are just starting a community. However, if you have a well-established community with fair revenue returns, you can pick up Heroku, and it's up to you and your balance sheet. But, I like how Heroku works, so I decided to learn the nuances of Heroku and Dokku and stick with Dokku.

Secondly, I also like the fact that their databases are attached differently from the core computation within Heroku's ecosystem. So, I decided to pick this feature too. So I installed a second droplet, namely dB droplet, for my databases.

Last but not least, the way we can update everything, be it my Forem or Databases. Dokku takes care of Forem if I just pushed the new fork, while Caprover does this for my databases. Many of you might have heard that installing Databases within Docker is not a good idea; that is true because the databases are supposed to be persistent. Caprover solves this part of the issue too. Also, as I don't want to risk my dB droplet, I'm paying extra money for its backup.

So, now I have a separate isolated and fail-safe database(I even added a load balancer, but I'm skipping that part) with a powerful forem droplet for handling the RAM hungry sidekiq_worker. I'm not elaborating this much, but by configuring MALLOC_ARENA, WEB_CURRENCY, HEAP_GROWTH_FACTOR, and Jemalloc, we can optimise our hunger sidekiq_worker. You can also limit RAM, and there is a lot of auto management you can do for more optimisation.

As this is already a long post, I decided to write a new article for step by step instructions, but it might take a while and as I intended to make it my first article in [Leewardslope](https://app.leewardslope.com/).

## Our Future

*   We never had funding, and every penny comes from the self-investment of the team.

*   We don't have an official developer, but we rely on Forem for that.

*   We don't have a stable educators base, but everyone in our team is an expert in their field.

*   We don't have a source of income, but we are pursuing our dreams to change our surroundings.

We might be a few college graduates, but many people need us. So what else do we need for motivation to move forward?

Today we are one step ahead of yesterday because of Forem. We also hope that Forem will help many other dream communities to life. This open-source project is one of the best examples to show how a small change can make a difference in our interactions with our communities. The possibilities of the emergence of new communities are endless, and Leewardslope is one among them.
